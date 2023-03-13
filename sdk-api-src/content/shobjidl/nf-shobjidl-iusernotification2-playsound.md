---
UID: NF:shobjidl.IUserNotification2.PlaySound
title: IUserNotification2::PlaySound (shobjidl.h)
description: Plays a sound in conjunction with the notification. (IUserNotification2.PlaySound)
helpviewer_keywords: ["IUserNotification2 interface [Windows Shell]","PlaySound method","IUserNotification2.PlaySound","IUserNotification2::PlaySound","PlaySound","PlaySound method [Windows Shell]","PlaySound method [Windows Shell]","IUserNotification2 interface","_shell_IUserNotification2_PlaySound","shell.IUserNotification2_PlaySound","shobjidl/IUserNotification2::PlaySound"]
old-location: shell\IUserNotification2_PlaySound.htm
tech.root: shell
ms.assetid: C1C0C408-B860-4aa6-8696-C95BF73AAB54
ms.date: 12/05/2018
ms.keywords: IUserNotification2 interface [Windows Shell],PlaySound method, IUserNotification2.PlaySound, IUserNotification2::PlaySound, PlaySound, PlaySound method [Windows Shell], PlaySound method [Windows Shell],IUserNotification2 interface, _shell_IUserNotification2_PlaySound, shell.IUserNotification2_PlaySound, shobjidl/IUserNotification2::PlaySound
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IUserNotification2::PlaySound
 - shobjidl/IUserNotification2::PlaySound
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IUserNotification2.PlaySound
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

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The string pointed to by <i>pszSoundName</i> contains an alias for a system event found in the registry or the Win.ini file; for instance, "SystemExit".

The specified sound is played asynchronously and the method returns immediately after beginning the sound. To stop an asynchronous waveform sound, call <b>IUserNotification2::PlaySound</b> with <i>pszSoundName</i> set to <b>NULL</b>.

The specified sound event will yield to another sound event that is already playing. If a sound cannot be played because the resource needed to play that sound is busy, the method immediately returns S_FALSE without playing the requested sound.

If the specified sound cannot be found, <b>IUserNotification2::PlaySound</b> uses the system default sound.

## -see-also

<a href="/windows/desktop/api/shobjidl/nn-shobjidl-iusernotification2">IUserNotification2</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iusernotification-playsound">PlaySound</a>
