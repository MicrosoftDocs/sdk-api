---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _AUDIO_STREAM_CATEGORY enumeration


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




<a href="https://msdn.microsoft.com/7d25be71-ffbe-4e8c-9a45-cdeb35d10292">Core Audio Enumerations</a>
 

 

