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

# XMConvertFloatToHalfStream function


## -description


Converts a stream of single-precision floating-point values to a stream of half-precision floating-point values.


## -parameters




### -param pOutputStream [out]

Address of the first <b>HALF</b> value in the output stream.


### -param OutputStride [in]

Stride in bytes between the <b>HALF</b> values in the output stream.


### -param pInputStream [in]

Address of the first <b>float</b> value in the input stream.


### -param InputStride [in]

Stride in bytes between the <b>float</b> values in the input stream.


### -param FloatCount [in]

Number of <b>float</b> values to convert.


## -returns



Returns the address of the first <b>HALF</b> value in the output stream.




## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/6a0a8422-991d-00aa-0fd7-b41387adc72e">DirectXMath Library Conversion Functions</a>



<a href="https://msdn.microsoft.com/463abe18-b8c4-44be-9740-b7e0459d3ebd">XMConvertFloatToHalf</a>
 

 

