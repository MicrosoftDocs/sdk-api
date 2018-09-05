---
UID: NF:audioclient.IAudioClient2.GetBufferSizeLimits
title: IAudioClient2::GetBufferSizeLimits
author: windows-sdk-content
description: The GetBufferSizeLimits method returns the buffer size limits of the hardware audio engine in 100-nanosecond units.
old-location: coreaudio\iaudioclient2_getbuffersizelimits.htm
old-project: CoreAudio
ms.assetid: BCB6066E-2672-4E56-83EA-7EBEC3C7F3DD
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: GetBufferSizeLimits, GetBufferSizeLimits method [Core Audio], GetBufferSizeLimits method [Core Audio],IAudioClient2 interface, IAudioClient2 interface [Core Audio],GetBufferSizeLimits method, IAudioClient2.GetBufferSizeLimits, IAudioClient2::GetBufferSizeLimits, audioclient/IAudioClient2::GetBufferSizeLimits, coreaudio.getbuffersizelimits_iaudioclient2__getbuffersizelimits, coreaudio.iaudioclient2_getbuffersizelimits
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: audioclient.h
req.include-header: 
req.redist: 
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
 - IAudioClient2.GetBufferSizeLimits
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioClient2::GetBufferSizeLimits


## -description


The <b>GetBufferSizeLimits</b> method returns the buffer size limits of the hardware audio engine in 100-nanosecond units.


## -parameters




### -param pFormat [in]

A pointer to the target format that is being queried for the buffer size limit.


### -param bEventDriven [in]

Boolean value to indicate whether or not the stream can be event-driven.


### -param phnsMinBufferDuration [out]

Returns a pointer to the minimum buffer size (in 100-nanosecond units) that is 
required for the underlying hardware audio engine to operate at the format specified  in the <i>pFormat</i> parameter,  without frequent audio glitching.


### -param phnsMaxBufferDuration [out]

Returns a pointer to the maximum buffer size (in 100-nanosecond units) that the underlying hardware 
audio engine can support for the format specified  in the <i>pFormat</i> parameter.



## -returns



The <b>GetBufferSizeLimits</b> method returns <b>S_OK</b> to indicate that it has completed successfully. Otherwise it returns an appropriate error code. For example, it can return <b>AUDCLNT_E_DEVICEINVALIDATED</b>, if the device was removed and the method is called.




## -remarks



The <b>GetBufferSizeLimits</b> method is a device-facing method    
and does not require prior audio stream initialization.




## -see-also




<a href="https://msdn.microsoft.com/9CE79CEB-115E-4802-A687-B2CB23E6A0E0">IAudioClient2</a>
 

 

