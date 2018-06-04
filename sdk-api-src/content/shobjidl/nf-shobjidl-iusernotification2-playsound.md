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

# IUserNotification2::PlaySound


## -description


Plays a sound in conjunction with the notification.


## -parameters




### -param pszSoundName [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated Unicode string that specifies the alias of the sound file to play.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The string pointed to by <i>pszSoundName</i> contains an alias for a system event found in the registry or the Win.ini file; for instance, "SystemExit".

The specified sound is played asynchronously and the method returns immediately after beginning the sound. To stop an asynchronous waveform sound, call <b>IUserNotification2::PlaySound</b> with <i>pszSoundName</i> set to <b>NULL</b>.

The specified sound event will yield to another sound event that is already playing. If a sound cannot be played because the resource needed to play that sound is busy, the method immediately returns S_FALSE without playing the requested sound.

If the specified sound cannot be found, <b>IUserNotification2::PlaySound</b> uses the system default sound.




## -see-also




<a href="https://msdn.microsoft.com/6605a014-4f79-4856-8fd9-df926ea76052">IUserNotification2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965711">PlaySound</a>
 

 

