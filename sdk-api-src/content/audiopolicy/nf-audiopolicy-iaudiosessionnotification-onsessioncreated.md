---
UID: NF:audiopolicy.IAudioSessionNotification.OnSessionCreated
title: IAudioSessionNotification::OnSessionCreated
author: windows-sdk-content
description: The OnSessionCreated method notifies the registered processes that the audio session has been created.
old-location: coreaudio\iaudiosessionnotification_onsessioncreated.htm
old-project: CoreAudio
ms.assetid: 03f22e06-f446-4c57-a955-3d12deec4152
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IAudioSessionNotification interface [Core Audio],OnSessionCreated method, IAudioSessionNotification.OnSessionCreated, IAudioSessionNotification::OnSessionCreated, OnSessionCreated, OnSessionCreated method [Core Audio], OnSessionCreated method [Core Audio],IAudioSessionNotification interface, audiopolicy/IAudioSessionNotification::OnSessionCreated, coreaudio.iaudiosessionnotification_onsessioncreated
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: audiopolicy.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: UNCOMPRESSEDAUDIOFORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - audiopolicy.h
api_name:
 - IAudioSessionNotification.OnSessionCreated
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioSessionNotification::OnSessionCreated


## -description


The <b>OnSessionCreated</b> method notifies the registered processes that the audio session has been created.
      


## -parameters




### -param NewSession [in]

Pointer to the <a href="https://msdn.microsoft.com/4446140e-2e61-40ed-b0f9-4c1b90e7c2de">IAudioSessionControl</a> interface of the audio session that was created.


## -returns



If the method succeeds, it returns S_OK.
          




## -remarks



After registering its <a href="https://msdn.microsoft.com/69222168-87d7-4f5a-93b1-6d91263a54bd">IAudioSessionNotification</a> interface, the application receives event notifications in the form of callbacks through the methods of the interface.

The audio engine calls <b>OnSessionCreated</b> when a new session is activated on the device endpoint.
This method is called from the session manager thread.  This method must take a reference to the session in the <i>NewSession</i> parameter if it wants to keep the reference after this call completes.




## -see-also




<a href="https://msdn.microsoft.com/69222168-87d7-4f5a-93b1-6d91263a54bd">IAudioSessionNotification</a>
 

 

