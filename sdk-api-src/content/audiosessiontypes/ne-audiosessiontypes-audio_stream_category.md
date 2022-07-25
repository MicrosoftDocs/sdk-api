---
UID: NE:audiosessiontypes._AUDIO_STREAM_CATEGORY
title: AUDIO_STREAM_CATEGORY (audiosessiontypes.h)
description: Specifies the category of an audio stream.
helpviewer_keywords: ["AUDIO_STREAM_CATEGORY","AUDIO_STREAM_CATEGORY enumeration [Core Audio]","AudioCategory_Alerts","AudioCategory_BackgroundCapableMedia","AudioCategory_Communications","AudioCategory_ForegroundOnlyMedia","AudioCategory_GameChat","AudioCategory_GameEffects","AudioCategory_GameMedia","AudioCategory_Media","AudioCategory_Movie","AudioCategory_Other","AudioCategory_SoundEffects","AudioCategory_Speech","audiosessiontypes/AUDIO_STREAM_CATEGORY","audiosessiontypes/AudioCategory_Alerts","audiosessiontypes/AudioCategory_BackgroundCapableMedia","audiosessiontypes/AudioCategory_Communications","audiosessiontypes/AudioCategory_ForegroundOnlyMedia","audiosessiontypes/AudioCategory_GameChat","audiosessiontypes/AudioCategory_GameEffects","audiosessiontypes/AudioCategory_GameMedia","audiosessiontypes/AudioCategory_Media","audiosessiontypes/AudioCategory_Movie","audiosessiontypes/AudioCategory_Other","audiosessiontypes/AudioCategory_SoundEffects","audiosessiontypes/AudioCategory_Speech","coreaudio.audio_stream_category"]
old-location: coreaudio\audio_stream_category.htm
tech.root: CoreAudio
ms.assetid: B6B9195A-2704-4633-AFCF-B01CED6B6DB4
ms.date: 12/05/2018
ms.keywords: AUDIO_STREAM_CATEGORY, AUDIO_STREAM_CATEGORY enumeration [Core Audio], AudioCategory_Alerts, AudioCategory_BackgroundCapableMedia, AudioCategory_Communications, AudioCategory_ForegroundOnlyMedia, AudioCategory_GameChat, AudioCategory_GameEffects, AudioCategory_GameMedia, AudioCategory_Media, AudioCategory_Movie, AudioCategory_Other, AudioCategory_SoundEffects, AudioCategory_Speech, audiosessiontypes/AUDIO_STREAM_CATEGORY, audiosessiontypes/AudioCategory_Alerts, audiosessiontypes/AudioCategory_BackgroundCapableMedia, audiosessiontypes/AudioCategory_Communications, audiosessiontypes/AudioCategory_ForegroundOnlyMedia, audiosessiontypes/AudioCategory_GameChat, audiosessiontypes/AudioCategory_GameEffects, audiosessiontypes/AudioCategory_GameMedia, audiosessiontypes/AudioCategory_Media, audiosessiontypes/AudioCategory_Movie, audiosessiontypes/AudioCategory_Other, audiosessiontypes/AudioCategory_SoundEffects, audiosessiontypes/AudioCategory_Speech, coreaudio.audio_stream_category
req.header: audiosessiontypes.h
req.include-header: Audioclient.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: AUDIO_STREAM_CATEGORY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AUDIO_STREAM_CATEGORY
 - audiosessiontypes/_AUDIO_STREAM_CATEGORY
 - AUDIO_STREAM_CATEGORY
 - audiosessiontypes/AUDIO_STREAM_CATEGORY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - audiosessiontypes.h
api_name:
 - AUDIO_STREAM_CATEGORY
---

# AUDIO_STREAM_CATEGORY enumeration


## -description

Specifies the category of an audio stream.

## -enum-fields

### -field AudioCategory_Other

Other audio stream.

### -field AudioCategory_ForegroundOnlyMedia

Media that will only stream when the app is in the foreground. This enumeration value has been deprecated. For more information, see the Remarks section.

### -field AudioCategory_BackgroundCapableMedia

Media that can be streamed when the app is in the background. This enumeration value has been deprecated. For more information, see the Remarks section.

### -field AudioCategory_Communications

Real-time communications, such as VOIP or chat.

### -field AudioCategory_Alerts

Alert sounds.

### -field AudioCategory_SoundEffects

Sound effects.

### -field AudioCategory_GameEffects

Game sound effects.

### -field AudioCategory_GameMedia

Background audio for games.

### -field AudioCategory_GameChat

Game chat audio. Similar to <b>AudioCategory_Communications</b> except that <b>AudioCategory_GameChat</b> will not attenuate other streams.

### -field AudioCategory_Speech

Speech.

### -field AudioCategory_Movie

Stream that includes audio with dialog.

### -field AudioCategory_Media

Stream that includes audio without dialog.

### -field AudioCategory_FarFieldSpeech

Media is audio captured with the intent of capturing voice sources located in the ‘far field’. (Far away from the microphone.)

### -field AudioCategory_UniformSpeech

Media is captured audio that requires consistent speech processing for the captured audio stream across all Windows devices. Used by applications that process speech data using machine learning algorithms.


### -field AudioCategory_VoiceTyping

Media is audio captured with the intent of enabling dictation or typing by voice. 

## -remarks

Note that only a subset of the audio stream categories are valid for certain stream types.

<table>
<tr>
<th>Stream type</th>
<th>Valid categories</th>
</tr>
<tr>
<td>Render stream</td>
<td>All categories are valid.</td>
</tr>
<tr>
<td>Capture stream</td>
<td>AudioCategory_Communications, AudioCategory_Speech, AudioCategory_Other</td>
</tr>
<tr>
<td>Loopback stream</td>
<td>AudioCategory_Other</td>
</tr>
</table>
 

Games should categorize their music streams as <b>AudioCategory_GameMedia</b> so that game music mutes automatically if another application plays music in the background. Music or video applications should categorize their streams as <b>AudioCategory_Media</b> or <b>AudioCategory_Movie</b> so they will take priority over <b>AudioCategory_GameMedia</b> streams. Game audio for in-game cinematics or cutscenes, when the audio is premixed or for creative reasons should take priority over background audio, should also be categorized as <b>Media</b> or <b>Movie</b>.

The values <b>AudioCategory_ForegroundOnlyMedia</b> and <b>AudioCategory_BackgroundCapableMedia</b> are deprecated. For Windows Store apps, these values will continue to function the same when running on Windows 10 as they did on Windows 8.1. Attempting to use these values in a Universal Windows Platform (UWP) app, will result in compilation errors and an exception at runtime. Using these values in a Windows desktop application built with the Windows 10   SDK the  will result in a compilation error.

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-enumerations">Core Audio Enumerations</a>