---
UID: NF:directxpackedvector.XMConvertFloatToHalfStream
title: XMConvertFloatToHalfStream function
author: windows-sdk-content
description: Converts a stream of single-precision floating-point values to a stream of half-precision floating-point values.
old-location: dxmath\xmconvertfloattohalfstream.htm
old-project: dxmath
ms.assetid: M:Microsoft.directx_sdk.conversion.XMConvertFloatToHalfStream(HALF@,uint32_t,const float,uint32_t,uint32_t)
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: DirectX::PackedVector.XMConvertFloatToHalfStream, XMConvertFloatToHalfStream, XMConvertFloatToHalfStream method [DirectX Math Support APIs], dxmath.xmconvertfloattohalfstream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: directxpackedvector.h
req.include-header: DirectXPackedVector.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: DirectX::PackedVector
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
 - directxpackedvector.h
api_name:
 - XMConvertFloatToHalfStream
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

