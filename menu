#include <stdio.h>
#include "SDL/SDL.h"
#include <SDL/SDL_image.h>
#include <SDL/SDL_ttf.h>
#include <SDL/SDL_getenv.h>
#include <SDL/SDL_mixer.h>

int main(int argc, char *argv[]){

char pause;


SDL_Event event;
SDL_Init ( SDL_INIT_VIDEO );
TTF_Init();
SDL_Surface *screen=SDL_SetVideoMode(1360,751,32, SDL_HWSURFACE|SDL_DOUBLEBUF|SDL_RESIZABLE);


if (!screen){
printf("unable to set video: %s \n", SDL_GetError());
return (-1);
}



//--------------------------------------------------------------------------------------
//--------------------------------------------------------------------------------------
//--------------------------------------------------------------------------------------
//--------------------------------------------------------------------------------------



SDL_Rect Background;
Background.x = 0;
Background.y = 0;
SDL_Rect rcontinuer;
rcontinuer.x=600;
rcontinuer.y=140;
SDL_Rect roption;
roption.x = 600;
roption.y=230;
SDL_Rect rquiter;
rquiter.x = 600;
rquiter.y=340;
SDL_Rect text;
text.x = 20;
text.y = 580;
SDL_Rect rretrun;
rretrun.x = 600;
rretrun.y=400;
SDL_Rect rfullscreen;
rfullscreen.x = 600;
rfullscreen.y=300;
SDL_Rect rvol;
rvol.x = 660;
rvol.y=200;
SDL_Rect rplus;
rplus.x = 600;
rplus.y=200;
SDL_Rect rless;
rless.x = 730;
rless.y=220;
SDL_Surface *bg = SDL_LoadBMP("Background3.bmp");
SDL_Surface *bg2 = SDL_LoadBMP("Background2.bmp");
SDL_Surface *continuer = SDL_LoadBMP("newgame.bmp");
SDL_Surface *option = SDL_LoadBMP("options.bmp");
SDL_Surface *quiter = SDL_LoadBMP("quit.bmp");
SDL_Surface *retour = SDL_LoadBMP("back.bmp");
SDL_Surface *continuer1 = SDL_LoadBMP("newgame2.bmp");
SDL_Surface *option1 = SDL_LoadBMP("options2.bmp");
SDL_Surface *quiter1 = SDL_LoadBMP("quit2.bmp");
SDL_Surface *retour1 = SDL_LoadBMP("back2.bmp");
SDL_Surface *fullscreen = SDL_LoadBMP("fullscreen.bmp");
SDL_Surface *fullscreen1 = SDL_LoadBMP("fullscreen2.bmp");
SDL_Surface *vol = SDL_LoadBMP("vol.bmp");
SDL_Surface *vol1 = SDL_LoadBMP("vol2.bmp");
SDL_Surface *vol2 = SDL_LoadBMP("vol3.bmp");
SDL_Surface *mute = SDL_LoadBMP("mute.bmp");
SDL_Surface *plus = SDL_LoadBMP("plus.bmp");
SDL_Surface *less = SDL_LoadBMP("less.bmp");
SDL_SetColorKey(bg, SDL_SRCCOLORKEY, SDL_MapRGB(bg->format, 0, 0, 255));
SDL_SetColorKey(bg2, SDL_SRCCOLORKEY, SDL_MapRGB(bg2->format, 0, 0, 255));
SDL_SetColorKey(continuer, SDL_SRCCOLORKEY, SDL_MapRGB(continuer->format, 0, 0, 0));
SDL_SetColorKey(option, SDL_SRCCOLORKEY, SDL_MapRGB(option->format, 0, 0, 0));
SDL_SetColorKey(quiter, SDL_SRCCOLORKEY, SDL_MapRGB(quiter->format, 0, 0, 0));
SDL_SetColorKey(retour, SDL_SRCCOLORKEY, SDL_MapRGB(retour->format, 0, 0, 0));
SDL_SetColorKey(continuer1, SDL_SRCCOLORKEY, SDL_MapRGB(continuer1->format, 0, 0, 0));
SDL_SetColorKey(option1, SDL_SRCCOLORKEY, SDL_MapRGB(option1->format, 0, 0, 0));
SDL_SetColorKey(quiter1, SDL_SRCCOLORKEY, SDL_MapRGB(quiter1->format, 0, 0, 0));
SDL_SetColorKey(retour1, SDL_SRCCOLORKEY, SDL_MapRGB(retour1->format, 0, 0, 0));
SDL_SetColorKey(fullscreen, SDL_SRCCOLORKEY, SDL_MapRGB(fullscreen->format, 0, 0, 0));
SDL_SetColorKey(fullscreen1, SDL_SRCCOLORKEY, SDL_MapRGB(fullscreen1->format, 0, 0, 0));
SDL_SetColorKey(vol, SDL_SRCCOLORKEY, SDL_MapRGB(vol->format, 0, 0, 0));
SDL_SetColorKey(vol1, SDL_SRCCOLORKEY, SDL_MapRGB(vol1->format, 0, 0, 0));
SDL_SetColorKey(vol2, SDL_SRCCOLORKEY, SDL_MapRGB(vol2->format, 0, 0, 0));
SDL_SetColorKey(mute, SDL_SRCCOLORKEY, SDL_MapRGB(mute->format, 0, 0, 0));
SDL_SetColorKey(plus, SDL_SRCCOLORKEY, SDL_MapRGB(plus->format, 0, 0, 0));
SDL_SetColorKey(less, SDL_SRCCOLORKEY, SDL_MapRGB(less->format, 0, 0, 0));

SDL_WM_SetCaption("The Savior",NULL);
SDL_Flip(screen);


SDL_Surface *texte =NULL;
TTF_Font *police = NULL;

int c=1;
SDL_Color couleurNoire = {127,127,127};
police = TTF_OpenFont("font xD.ttf", 130);
texte = TTF_RenderText_Blended(police, "The Savior", couleurNoire);

SDL_BlitSurface(bg, NULL, screen, &Background);
SDL_BlitSurface(continuer,NULL, screen, &rcontinuer);
SDL_BlitSurface(option,NULL, screen, &roption);
SDL_BlitSurface(quiter,NULL, screen, &rquiter);


//--------------------------------------------------------------------------------------
//--------------------------------------------------------------------------------------
//--------------------------------------------------------------------------------------
//--------------------------------------------------------------------------------------


if(Mix_OpenAudio(44100, MIX_DEFAULT_FORMAT, MIX_DEFAULT_CHANNELS,1024) == -1)
    {
        printf("%s",Mix_GetError());
    }

    Mix_Music *musique;
    musique = Mix_LoadMUS("music1.mp3");
 

Mix_Chunk * son;
son= Mix_LoadWAV( "select.wav" );
Mix_Chunk * effect;
effect= Mix_LoadWAV( "button.wav" );


int continu = 1;
int k=0,j=0,b=0,cc=0,pls=0,kekw=1,h=0;




//--------------------------------------------------------------------------------------
//--------------------------------------------------------------------------------------
//--------------------------------------------------------------------------------------
//--------------------------------------------------------------------------------------





    while (continu)
    {
		if(kekw==1)
	  Mix_PlayMusic(musique, -1);
     SDL_WaitEvent(&event);
		 switch(event.type)
          {
	case SDL_QUIT :
		continu = 0;
	break;

	case SDL_MOUSEMOTION:
		//new game 
		if ((event.motion.x>570)&&(event.motion.y>150)&&(event.motion.x<850)&&(event.motion.y<180))
                   	 j=1;
		// options
		else if (event.motion.x >575 && event.motion.y >210 && event.motion.x <760 && event.motion.y <290)
                	j=2;
		//quit
		else if ( event.motion.x >575 && event.motion.y >350 && event.motion.x < 750 && event.motion.y <400)
	                 j=3;
		//return
		else if ( event.motion.x >575 && event.motion.y >410 && event.motion.x < 750 && event.motion.y <460)
			{
				j=4;
			}
		//fullscreen
		else if ( event.motion.x >575 && event.motion.y >310 && event.motion.x < 750 && event.motion.y <360)
			{
				j=5;
			}
	
		else						
			j=0;	
		break;



	case SDL_MOUSEBUTTONDOWN:	
		// options press
		if (event.button.button == SDL_BUTTON_LEFT)
			if(event.motion.x >575 && event.motion.y >210 && event.motion.x <760 && event.motion.y <290)
			k=1; 
		// new game press
		else if (event.button.button == SDL_BUTTON_LEFT)
			if((event.motion.x>570)&&(event.motion.y>150)&&(event.motion.x<850)&&(event.motion.y<180))
			k=6; 
		// quit press
		else if (event.button.button == SDL_BUTTON_LEFT)
			if ( event.motion.x >575 && event.motion.y >350 && event.motion.x < 750 && event.motion.y <400)
				{
				Mix_PlayChannel( -1, effect, 0 );
				k=4;
				}
		// return press
			else if (event.button.button == SDL_BUTTON_LEFT)
			if ( event.motion.x >575 && event.motion.y >410 && event.motion.x < 750 && event.motion.y <460)
			{
				Mix_PlayChannel( -1, effect, 0 );
				k=2;
				b=0;
				cc=0;
				pls=0;
			}
		//volume + press
		else if (event.button.button == SDL_BUTTON_LEFT)
			if (event.motion.x >580 && event.motion.y >170 && event.motion.x < 620 && event.motion.y <220)
				k=3;
		//volume - press
		else if (event.button.button == SDL_BUTTON_LEFT)
			if (event.motion.x >710 && event.motion.y >210 && event.motion.x < 780 && event.motion.y <230)
				k=7;
		// fullscreen press
		else if (event.button.button == SDL_BUTTON_LEFT)
			if ( event.motion.x >575 && event.motion.y >310 && event.motion.x < 750 && event.motion.y <360)
				k=5;

		break;
	}


		// retour menu
		if((j==0)&&(k==0)||(k==2))
		{
			
			SDL_BlitSurface(bg, NULL, screen, &Background );
			SDL_BlitSurface(continuer,NULL, screen, &rcontinuer);
			SDL_BlitSurface(option,NULL, screen, &roption);
			SDL_BlitSurface(quiter,NULL, screen, &rquiter);
			SDL_BlitSurface (texte, NULL, screen, &text);
			SDL_Flip(screen);
			k=0;
		
		}
		//afficher contiuner1.2
		else if((j==1)&&(k==0))
		{
			 SDL_BlitSurface(continuer1,NULL, screen, &rcontinuer);
			Mix_PlayChannel( -1, son, 0 );
                   	 SDL_Flip(screen);
		}
		// afficher quiter1.2
		else if((j==3)&&(k==0))
		{
			 SDL_BlitSurface(quiter1,NULL, screen, &rquiter);
			Mix_PlayChannel( -1, son, 0 );
                   	 SDL_Flip(screen);
		}
		// afficher option1.2
		else if((j==2)&&(k==0))
		{
			 SDL_BlitSurface(option1,NULL, screen, &roption);
			Mix_PlayChannel( -1, son, 0 );
                   	 SDL_Flip(screen);

		}
		//quiter 
		else if((j==2)&&(k==4))
		{
			continu=0;
		}
		// entre option if vol=1
		else if((j==2)&&(k==1)&&(h==0))
		{
			
				
			if(cc==0)
			{
			Mix_PlayChannel( -1, effect, 0 );	
			cc++;
			}
			 SDL_BlitSurface(bg2, NULL, screen, &Background);
			SDL_BlitSurface(retour, NULL, screen, &rretrun);
			SDL_BlitSurface(fullscreen, NULL, screen, &rfullscreen);
			SDL_BlitSurface(vol, NULL, screen, &rvol);
			SDL_BlitSurface(plus, NULL, screen, &rplus);
			SDL_BlitSurface(less, NULL, screen, &rless);
			SDL_Flip(screen);
			pls=1;
					
		}
			// entre option if vol=2
		else if((j==2)&&(k==1)&&(h==1))
		{
			
				
			if(cc==0)
			{
			Mix_PlayChannel( -1, effect, 0 );	
			cc++;
			}
			 SDL_BlitSurface(bg2, NULL, screen, &Background);
			SDL_BlitSurface(retour, NULL, screen, &rretrun);
			SDL_BlitSurface(fullscreen, NULL, screen, &rfullscreen);
			SDL_BlitSurface(vol1, NULL, screen, &rvol);
			SDL_BlitSurface(plus, NULL, screen, &rplus);
			SDL_BlitSurface(less, NULL, screen, &rless);
			SDL_Flip(screen);
			pls=1;
					
		}
		// entre option if vol=3
		else if((j==2)&&(k==1)&&(h==2))
		{
			
				
			if(cc==0)
			{
			Mix_PlayChannel( -1, effect, 0 );	
			cc++;
			}
			 SDL_BlitSurface(bg2, NULL, screen, &Background);
			SDL_BlitSurface(retour, NULL, screen, &rretrun);
			SDL_BlitSurface(fullscreen, NULL, screen, &rfullscreen);
			SDL_BlitSurface(vol2, NULL, screen, &rvol);
			SDL_BlitSurface(plus, NULL, screen, &rplus);
			SDL_BlitSurface(less, NULL, screen, &rless);
			SDL_Flip(screen);
			pls=1;
					
		}
		// entre option if mute
		else if((j==2)&&(k==1)&&(h==3))
		{
			
				
			if(cc==0)
			{
			Mix_PlayChannel( -1, effect, 0 );	
			cc++;
			}
			 SDL_BlitSurface(bg2, NULL, screen, &Background);
			SDL_BlitSurface(retour, NULL, screen, &rretrun);
			SDL_BlitSurface(fullscreen, NULL, screen, &rfullscreen);
			SDL_BlitSurface(mute, NULL, screen, &rvol);
			SDL_BlitSurface(plus, NULL, screen, &rplus);
			SDL_BlitSurface(less, NULL, screen, &rless);
			SDL_Flip(screen);
			pls=1;
					
		}
		// refresh options if vol=1
		else if((j==0)&&(pls==1)&&(h==0))
		{
			
				
			 SDL_BlitSurface(bg2, NULL, screen, &Background);
			SDL_BlitSurface(retour, NULL, screen, &rretrun);
			SDL_BlitSurface(fullscreen, NULL, screen, &rfullscreen);
			SDL_BlitSurface(vol, NULL, screen, &rvol);
			SDL_BlitSurface(plus, NULL, screen, &rplus);
			SDL_BlitSurface(less, NULL, screen, &rless);
			SDL_Flip(screen);
			
					
		}
		// refresh options if vol=2
		else if((j==0)&&(pls==1)&&(h==1))
		{
			
				
			 SDL_BlitSurface(bg2, NULL, screen, &Background);
			SDL_BlitSurface(retour, NULL, screen, &rretrun);
			SDL_BlitSurface(fullscreen, NULL, screen, &rfullscreen);
			SDL_BlitSurface(vol1, NULL, screen, &rvol);
			SDL_BlitSurface(plus, NULL, screen, &rplus);
			SDL_BlitSurface(less, NULL, screen, &rless);
			SDL_Flip(screen);
			
					
		}
		// refresh options if vol=3
		else if((j==0)&&(pls==1)&&(h==2))
		{
			
				
			 SDL_BlitSurface(bg2, NULL, screen, &Background);
			SDL_BlitSurface(retour, NULL, screen, &rretrun);
			SDL_BlitSurface(fullscreen, NULL, screen, &rfullscreen);
			SDL_BlitSurface(vol2, NULL, screen, &rvol);
			SDL_BlitSurface(plus, NULL, screen, &rplus);
			SDL_BlitSurface(less, NULL, screen, &rless);
			SDL_Flip(screen);
			
					
		}
		// refresh options if mute
		else if((j==0)&&(pls==1)&&(h==3))
		{
			
				
			 SDL_BlitSurface(bg2, NULL, screen, &Background);
			SDL_BlitSurface(retour, NULL, screen, &rretrun);
			SDL_BlitSurface(fullscreen, NULL, screen, &rfullscreen);
			SDL_BlitSurface(mute, NULL, screen, &rvol);
			SDL_BlitSurface(plus, NULL, screen, &rplus);
			SDL_BlitSurface(less, NULL, screen, &rless);
			SDL_Flip(screen);
			
					
		}
			

		// afficher fullscreen1.2
		else if ((pls==1)&&(j==5))
		{
			SDL_BlitSurface(fullscreen1,NULL, screen, &rfullscreen);
			Mix_PlayChannel( -1, son, 0 );
                   	SDL_Flip(screen);
		}
		// afficher retun1.2
		else if ((pls==1)&&(j==4))
		{
			SDL_BlitSurface(retour1,NULL, screen, &rretrun);
			Mix_PlayChannel( -1, son, 0 );
                   	SDL_Flip(screen);
		}
		// afficher volume1.2
		else if ((pls==1)&&(j==7))
		{
				
				Mix_PlayChannel( -1, son, 0 );

                   		SDL_Flip(screen);
		}
		//click on volume - one time 
		else if ((pls==1)&&(k==7)&&(h==0))
			{
			SDL_BlitSurface(vol1, NULL, screen, &rvol);
                   	SDL_Flip(screen);
			Mix_VolumeMusic(MIX_MAX_VOLUME/2);
			Mix_VolumeChunk(son, MIX_MAX_VOLUME/2);
			Mix_VolumeChunk(effect, MIX_MAX_VOLUME/2);
			h=1;
			}
		//click on volume - two time 
		else if ((pls==1)&&(k==7)&&(h==1))
			{
			SDL_BlitSurface(vol2, NULL, screen, &rvol);
                   	SDL_Flip(screen);
			Mix_VolumeMusic(MIX_MAX_VOLUME/5);
			Mix_VolumeChunk(son, MIX_MAX_VOLUME/5);
			Mix_VolumeChunk(effect, MIX_MAX_VOLUME/5);
			h=2;
			}
		//click on volume - three time 
		else if ((pls==1)&&(k==7)&&(h==2))
			{
			SDL_BlitSurface(mute, NULL, screen, &rvol);
                   	SDL_Flip(screen);
			Mix_VolumeMusic(MIX_MAX_VOLUME/100000000);
			Mix_VolumeChunk(son, MIX_MAX_VOLUME/100000000);
			Mix_VolumeChunk(effect, MIX_MAX_VOLUME/10000000);
			h=3;
			}
		//click on volume + if clicked on - one time 
		else if ((pls==1)&&(k==3)&&(h==1))
			{
			SDL_BlitSurface(vol, NULL, screen, &rvol);
                   	SDL_Flip(screen);
			Mix_VolumeMusic(MIX_MAX_VOLUME/1);
			Mix_VolumeChunk(son, MIX_MAX_VOLUME/1);
			Mix_VolumeChunk(effect, MIX_MAX_VOLUME/1);
			h=0;
			}
		//click on volume + if clicked on - two times 
		else if ((pls==1)&&(k==3)&&(h==2))
			{
			SDL_BlitSurface(vol1, NULL, screen, &rvol);
                   	SDL_Flip(screen);
			Mix_VolumeMusic(MIX_MAX_VOLUME/2);
			Mix_VolumeChunk(son, MIX_MAX_VOLUME/2);
			Mix_VolumeChunk(effect, MIX_MAX_VOLUME/2);
			h=1;
			}
		//click on volume + if clicked on - three times
		else if ((pls==1)&&(k==3)&&(h==3))
			{
			SDL_BlitSurface(vol2, NULL, screen, &rvol);
                   	SDL_Flip(screen);
			Mix_VolumeMusic(MIX_MAX_VOLUME/5);
			Mix_VolumeChunk(son, MIX_MAX_VOLUME/5);
			Mix_VolumeChunk(effect, MIX_MAX_VOLUME/5);
			h=2;
			}
		// click on fullscreen
		else if ((pls==1)&&(k==5))
			{
			Mix_VolumeChunk(son, MIX_MAX_VOLUME/10000000);
			Mix_VolumeMusic(MIX_MAX_VOLUME/1000000000);
			Mix_VolumeChunk(effect, MIX_MAX_VOLUME/1000000000);	
			h=3;
		}
		


	kekw=0;
  }
    


pause=getchar();
SDL_FreeSurface(bg);
SDL_FreeSurface(bg2);
SDL_FreeSurface(continuer);
SDL_FreeSurface(continuer1);
SDL_FreeSurface(quiter);
SDL_FreeSurface(quiter1);
SDL_FreeSurface(option);
SDL_FreeSurface(option1);
SDL_FreeSurface(retour);
SDL_FreeSurface(retour1);
Mix_FreeMusic(musique);
Mix_FreeChunk(son);
Mix_FreeChunk(effect);
Mix_CloseAudio();
TTF_CloseFont(police);
TTF_Quit();
SDL_QUIT;

return 0;
}
