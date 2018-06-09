---
UID: NF:audioclient.IAudioClient2.SetClientProperties
title: IAudioClient2::SetClientProperties
author: windows-sdk-content
description: Sets the properties of the audio stream by populating an AudioClientProperties structure.
old-location: coreaudio\iaudioclient2_setclientproperties.htm
old-project: CoreAudio
ms.assetid: B9B98EF9-C0E1-430A-9C79-1B414F4D67B5
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IAudioClient2 interface [Core Audio],SetClientProperties method, IAudioClient2.SetClientProperties, IAudioClient2::SetClientProperties, SetClientProperties, SetClientProperties method [Core Audio], SetClientProperties method [Core Audio],IAudioClient2 interface, audioclient/IAudioClient2::SetClientProperties, coreaudio.iaudioclient2_setclientproperties
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: audioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioclient.h
api_name:
 - IAudioClient2.SetClientProperties
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioClient2::SetClientProperties


## -description


Sets the properties of the audio stream by populating an <a href="https://msdn.microsoft.com/5BCCD581-DB66-4939-A62A-2236B9E49AA7">AudioClientProperties</a> structure.


## -parameters




### -param pProperties [in]

Pointer to an <a href="https://msdn.microsoft.com/5BCCD581-DB66-4939-A62A-2236B9E49AA7">AudioClientProperties</a> structure.


## -returns



The <b>SetClientProperties</b> method returns <b>S_OK</b> to indicate that it has completed successfully. Otherwise it returns an appropriate error code.




## -remarks



Starting with Windows 10, hardware-offloaded audio streams must be event driven. This means that if you call <b>IAudioClient2::SetClientProperties</b> and set the <i>bIsOffload</i> parameter of the <a href="https://msdn.microsoft.com/5BCCD581-DB66-4939-A62A-2236B9E49AA7">AudioClientProperties</a> to TRUE, you must specify the <b>AUDCLNT_STREAMFLAGS_EVENTCALLBACK</b> flag in the <i>StreamFlags</i> parameter to <a href="https://msdn.microsoft.com/eb778503-06f8-4705-9f8d-9a4fd886ae27">IAudioClient::Initialize</a>.




## -see-also




<a href="https://msdn.microsoft.com/5BCCD581-DB66-4939-A62A-2236B9E49AA7">AudioClientProperties</a>



<a href="https://msdn.microsoft.com/9CE79CEB-115E-4802-A687-B2CB23E6A0E0">IAudioClient2</a>



<a href="https://msdn.microsoft.com/eb778503-06f8-4705-9f8d-9a4fd886ae27">IAudioClient::Initialize</a>
 

 

