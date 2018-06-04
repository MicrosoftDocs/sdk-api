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

# IWMReaderAdvanced2::Preroll


## -description



The <b>Preroll</b> method is used to begin prerolling (buffering data) for the reader.




## -parameters




### -param cnsStart [in]

Specifies the start time in 100-nanosecond units.


### -param cnsDuration [in]

Specifies the duration in 100-nanosecond units.


### -param fRate [in]

Specifies the data rate.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



This method can be called before the application calls <a href="https://msdn.microsoft.com/library/windows/hardware/hh973223">Start</a> to begin buffering data in advance. The parameters here must be set to the same values as those that are passed to <b>Start</b> when it is called. If the parameters are different, <b>Start</b> will do rebuffering.

It is important to allow sufficient time for the prerolling (buffering data) for the reader to be completed before calling <b>Start</b>. When prerolling local files, 6 seconds normally is sufficient. When prerolling files over the Internet, allow more time before calling <b>Start</b>. If insufficient time is allowed, the effect will be a longer <b>Start</b> time when <b>Start</b> is called.




## -see-also




<a href="https://msdn.microsoft.com/5d741e49-9fdf-4f8d-9ea1-faaecf879be4">IWMReaderAdvanced2 Interface</a>
 

 

