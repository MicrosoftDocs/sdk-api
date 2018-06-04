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

# IMFContentProtectionDevice::InvokeFunction


## -description


Calls into the implementation of the protection system in the security processor. 


## -parameters




### -param FunctionId [in]

The identifier of the function that you want to run. This identifier is defined by the implementation of the protection system.


### -param InputBufferByteCount [in]

The number of bytes of in the buffer that <i>InputBuffer</i> specifies, including private data.


### -param InputBuffer [in]

A pointer to the data that you want to provide as input.


### -param OutputBufferByteCount [in, out]

Pointer to a value that specifies the length in bytes of the data that the function wrote to the buffer that <i>OutputBuffer</i> specifies, including the private data.   
     


### -param OutputBuffer [out]

Pointer to the buffer where you want the function to write its output.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/A95F6526-60D2-4922-897E-6369EBB0DC79">IMFContentProtectionDevice</a>
 

 

