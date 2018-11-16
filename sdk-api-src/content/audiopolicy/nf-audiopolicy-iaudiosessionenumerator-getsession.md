---
UID: NF:audiopolicy.IAudioSessionEnumerator.GetSession
title: IAudioSessionEnumerator::GetSession
author: windows-sdk-content
description: The GetSession method gets the audio session specified by an audio session number.
old-location: coreaudio\iaudiosessionenumerator_getsession.htm
tech.root: CoreAudio
ms.assetid: 45b7af16-aca0-49f8-b977-f7e4f1885687
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetSession, GetSession method [Core Audio], GetSession method [Core Audio],IAudioSessionEnumerator interface, IAudioSessionEnumerator interface [Core Audio],GetSession method, IAudioSessionEnumerator.GetSession, IAudioSessionEnumerator::GetSession, audiopolicy/IAudioSessionEnumerator::GetSession, coreaudio.iaudiosessionenumerator_getsession
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: audiopolicy.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - audiopolicy.h
api_name:
 - IAudioSessionEnumerator.GetSession
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- audiopolicy.h
: 
- IAudioSessionEnumerator.GetSession
: 
---

# IAudioSessionEnumerator::GetSession


## -description


The <b>GetSession</b> method gets the audio session specified by an audio session number.


## -parameters




### -param SessionCount [in]

The session number. If there are <i>n</i> sessions, the sessions are numbered from 0 to <i>n</i> – 1. To get the number of sessions, call the <a href="https://msdn.microsoft.com/a1fbfbf5-a79b-40bc-97c7-a76a181bbfec">IAudioSessionEnumerator::GetCount</a> method.




### -param Session [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/4446140e-2e61-40ed-b0f9-4c1b90e7c2de">IAudioSessionControl</a> interface of the session object in the collection that is maintained by the session enumerator. The caller must release the interface pointer.


## -returns



If the method succeeds, it returns S_OK.




## -see-also




<a href="https://msdn.microsoft.com/a7976d13-3391-4747-b83a-cfb9407b34f2">IAudioSessionEnumerator</a>
 

 

