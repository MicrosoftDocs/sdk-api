---
UID: NE:portabledevice.tagWPD_META_GENRES
title: tagWPD_META_GENRES
author: windows-driver-content
description: The WPD_META_GENRES enumeration type describes a broad genre type of a media file.
old-location: wpdsdk\wpd_meta_genres.htm
old-project: wpd_sdk
ms.assetid: a69cab70-5a45-4e75-abbd-230396c2b5ec
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: WPD_META_GENRES, WPD_META_GENRES enumeration [Windows Portable Devices SDK], WPD_META_GENRE_AUDIO_PODCAST, WPD_META_GENRE_FEATURE_FILM_VIDEO_FILE, WPD_META_GENRE_GENERIC_MUSIC_AUDIO_FILE, WPD_META_GENRE_GENERIC_NON_AUDIO_NON_VIDEO, WPD_META_GENRE_GENERIC_NON_MUSIC_AUDIO_FILE, WPD_META_GENRE_GENERIC_VIDEO_FILE, WPD_META_GENRE_HOME_VIDEO_FILE, WPD_META_GENRE_MIXED_PODCAST, WPD_META_GENRE_MUSIC_VIDEO_FILE, WPD_META_GENRE_NEWS_VIDEO_FILE, WPD_META_GENRE_PHOTO_MONTAGE_VIDEO_FILE, WPD_META_GENRE_SPOKEN_WORD_AUDIO_BOOK_FILES, WPD_META_GENRE_SPOKEN_WORD_FILES_NON_AUDIO_BOOK, WPD_META_GENRE_SPOKEN_WORD_NEWS, WPD_META_GENRE_SPOKEN_WORD_TALK_SHOWS, WPD_META_GENRE_TELEVISION_VIDEO_FILE, WPD_META_GENRE_TRAINING_EDUCATIONAL_VIDEO_FILE, WPD_META_GENRE_UNUSED, WPD_META_GENRE_VIDEO_PODCAST, enumeration [Windows Portable Devices SDK], portabledevice/WPD_META_GENRES, portabledevice/WPD_META_GENRE_AUDIO_PODCAST, portabledevice/WPD_META_GENRE_FEATURE_FILM_VIDEO_FILE, portabledevice/WPD_META_GENRE_GENERIC_MUSIC_AUDIO_FILE, portabledevice/WPD_META_GENRE_GENERIC_NON_AUDIO_NON_VIDEO, portabledevice/WPD_META_GENRE_GENERIC_NON_MUSIC_AUDIO_FILE, portabledevice/WPD_META_GENRE_GENERIC_VIDEO_FILE, portabledevice/WPD_META_GENRE_HOME_VIDEO_FILE, portabledevice/WPD_META_GENRE_MIXED_PODCAST, portabledevice/WPD_META_GENRE_MUSIC_VIDEO_FILE, portabledevice/WPD_META_GENRE_NEWS_VIDEO_FILE, portabledevice/WPD_META_GENRE_PHOTO_MONTAGE_VIDEO_FILE, portabledevice/WPD_META_GENRE_SPOKEN_WORD_AUDIO_BOOK_FILES, portabledevice/WPD_META_GENRE_SPOKEN_WORD_FILES_NON_AUDIO_BOOK, portabledevice/WPD_META_GENRE_SPOKEN_WORD_NEWS, portabledevice/WPD_META_GENRE_SPOKEN_WORD_TALK_SHOWS, portabledevice/WPD_META_GENRE_TELEVISION_VIDEO_FILE, portabledevice/WPD_META_GENRE_TRAINING_EDUCATIONAL_VIDEO_FILE, portabledevice/WPD_META_GENRE_UNUSED, portabledevice/WPD_META_GENRE_VIDEO_PODCAST, tagWPD_META_GENRES, wpdsdk.wpd_meta_genres
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: portabledevice.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Pnpxassoc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WPD_META_GENRES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	PortableDevice.h
api_name:
-	WPD_META_GENRES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# tagWPD_META_GENRES enumeration


## -description



        The <b>WPD_META_GENRES</b> enumeration type describes a broad genre type of a media file.
      


## -enum-fields




### -field WPD_META_GENRE_UNUSED


            The genre has not been set, or is not applicable.
          


### -field WPD_META_GENRE_GENERIC_MUSIC_AUDIO_FILE


            This is a generic music file (audio only).
          


### -field WPD_META_GENRE_GENERIC_NON_MUSIC_AUDIO_FILE


            This is a generic non-music audio file, for example, a speech or audio book.
          


### -field WPD_META_GENRE_SPOKEN_WORD_AUDIO_BOOK_FILES


            This is an audio book file.
          


### -field WPD_META_GENRE_SPOKEN_WORD_FILES_NON_AUDIO_BOOK


            This is a spoken-word audio file that is not an audio book, for example, an interview or speech.
          


### -field WPD_META_GENRE_SPOKEN_WORD_NEWS


            This is a news audio or video file.
          


### -field WPD_META_GENRE_SPOKEN_WORD_TALK_SHOWS


            This is an audio recording of a talk show.
          


### -field WPD_META_GENRE_GENERIC_VIDEO_FILE


            This is a generic video file.
          


### -field WPD_META_GENRE_NEWS_VIDEO_FILE


            This is a news video file.
          


### -field WPD_META_GENRE_MUSIC_VIDEO_FILE


            This is a music video file.
          


### -field WPD_META_GENRE_HOME_VIDEO_FILE


            This is a home video file.
          


### -field WPD_META_GENRE_FEATURE_FILM_VIDEO_FILE


            This is a feature film video file.
          


### -field WPD_META_GENRE_TELEVISION_VIDEO_FILE


            This is a television program video file.
          


### -field WPD_META_GENRE_TRAINING_EDUCATIONAL_VIDEO_FILE


            This is an educational video file.
          


### -field WPD_META_GENRE_PHOTO_MONTAGE_VIDEO_FILE


            This is a video file featuring a photo montage.
          


### -field WPD_META_GENRE_GENERIC_NON_AUDIO_NON_VIDEO


            This is a file without audio or video.
          


### -field WPD_META_GENRE_AUDIO_PODCAST


            This is an audio podcast.
          


### -field WPD_META_GENRE_VIDEO_PODCAST


            This is a video podcast.
          


### -field WPD_META_GENRE_MIXED_PODCAST


            This is a podcast containing both audio and video.
          


## -remarks




        This enumeration is used by the <a href="media_properties.htm">WPD_MEDIA_META_GENRE</a> property.
      




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff597672">Structures and Enumeration Types</a>
 

 

