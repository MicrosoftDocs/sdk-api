---
UID: NF:shobjidl_core.IUserNotification.PlaySound
title: IUserNotification::PlaySound (shobjidl_core.h)
description: Plays a sound in conjunction with the notification. (IUserNotification.PlaySound)
helpviewer_keywords: ["IUserNotification interface [Windows Shell]","PlaySound method","IUserNotification.PlaySound","IUserNotification::PlaySound","PlaySound","PlaySound method [Windows Shell]","PlaySound method [Windows Shell]","IUserNotification interface","inet_IUserNotification_PlaySound","shell.IUserNotification_PlaySound","shobjidl_core/IUserNotification::PlaySound"]
old-location: shell\IUserNotification_PlaySound.htm
tech.root: shell
ms.assetid: 3d7533c8-3b52-42dd-bfaa-2305bf3b0b18
ms.date: 12/05/2018
ms.keywords: IUserNotification interface [Windows Shell],PlaySound method, IUserNotification.PlaySound, IUserNotification::PlaySound, PlaySound, PlaySound method [Windows Shell], PlaySound method [Windows Shell],IUserNotification interface, inet_IUserNotification_PlaySound, shell.IUserNotification_PlaySound, shobjidl_core/IUserNotification::PlaySound
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUserNotification::PlaySound
 - shobjidl_core/IUserNotification::PlaySound
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IUserNotification.PlaySound
---

# IUserNotification::PlaySound


## -description

Plays a sound in conjunction with the notification.

## -parameters

### -param pszSoundName [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated Unicode string that specifies the alias of the sound file to play.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The string pointed to by <i>pszSoundNamepqc</i> contains an alias for a system event found in the registry or the Win.ini file; for instance, "SystemExit".

The specified sound is played asynchronously and the method returns immediately after beginning the sound. To stop an asynchronous waveform sound, call <b>IUserNotification::PlaySound</b> with <i>pszSoundNamepqc</i> set to <b>NULL</b>.

The specified sound event will yield to another sound event that is already playing. If a sound cannot be played because the resource needed to play that sound is busy, the method immediately returns S_FALSE without playing the requested sound.

If the specified sound cannot be found, <b>IUserNotification::PlaySound</b> uses the system default sound.

