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
 

 

