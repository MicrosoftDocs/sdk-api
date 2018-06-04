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

# IUserNotification::PlaySound


## -description


Plays a sound in conjunction with the notification.


## -parameters




### -param pszSoundName






#### - pszSoundNamepqc [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated Unicode string that specifies the alias of the sound file to play.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The string pointed to by <i>pszSoundNamepqc</i> contains an alias for a system event found in the registry or the Win.ini file; for instance, "SystemExit".

The specified sound is played asynchronously and the method returns immediately after beginning the sound. To stop an asynchronous waveform sound, call <b>IUserNotification::PlaySound</b> with <i>pszSoundNamepqc</i> set to <b>NULL</b>.

The specified sound event will yield to another sound event that is already playing. If a sound cannot be played because the resource needed to play that sound is busy, the method immediately returns S_FALSE without playing the requested sound.

If the specified sound cannot be found, <b>IUserNotification::PlaySound</b> uses the system default sound.



