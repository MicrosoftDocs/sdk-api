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

# D3D11_TRACE_GS_INPUT_PRIMITIVE enumeration


## -description


Identifies the type of geometry shader input primitive.


## -enum-fields




### -field D3D11_TRACE_GS_INPUT_PRIMITIVE_UNDEFINED

Identifies the geometry shader input primitive as undefined.


### -field D3D11_TRACE_GS_INPUT_PRIMITIVE_POINT

Identifies the geometry shader input primitive as a point.


### -field D3D11_TRACE_GS_INPUT_PRIMITIVE_LINE

Identifies the geometry shader input primitive as a line.


### -field D3D11_TRACE_GS_INPUT_PRIMITIVE_TRIANGLE

Identifies the geometry shader input primitive as a triangle.


### -field D3D11_TRACE_GS_INPUT_PRIMITIVE_LINE_ADJ

Identifies the geometry shader input primitive as an adjacent line.


### -field D3D11_TRACE_GS_INPUT_PRIMITIVE_TRIANGLE_ADJ

Identifies the geometry shader input primitive as an adjacent triangle.


## -remarks



<b>D3D11_TRACE_GS_INPUT_PRIMITIVE</b> identifies the type of geometry shader input primitive in a <a href="https://msdn.microsoft.com/E4E44F7F-3760-490D-9BA3-677F63B93AA6">D3D11_TRACE_STATS</a> structure.

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/068ce652-8596-4492-992c-658d1fcf8a2c">Shader Enumerations</a>
 

 

