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

# D3D11_PIXEL_SHADER_TRACE_DESC structure


## -description


Describes an instance of a pixel shader to trace.


## -struct-fields




### -field Invocation

The invocation number of the instance of the pixel shader.


### -field X

The x-coordinate of the pixel.


### -field Y

The y-coordinate of the pixel.


### -field SampleMask

A value that describes a mask of pixel samples to trace. If this value specifies any of the masked samples, the trace is activated.  The least significant bit (LSB) is sample 0.  The non-multisample antialiasing (MSAA) counts as a sample count of 1; therefore, the LSB of <b>SampleMask</b> should be set. If set to zero, the pixel is not traced. However, pixel traces can still be enabled on an invocation basis.


## -remarks



This API requires the Windows Software Development Kit (SDK) for Windows 8.




## -see-also




<a href="https://msdn.microsoft.com/3b8ece5c-5065-4711-b12c-06cf7ea0e1ba">Shader Structures</a>
 

 

