---
UID: NE:strmif.CompressionCaps
title: CompressionCaps
author: windows-sdk-content
description: Indicates video compression capabilities.
old-location: dshow\compressioncaps.htm
tech.root: DirectShow
ms.assetid: e964756f-1c60-42fd-8497-637d5fc005d7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CompressionCaps, CompressionCaps enumeration [DirectShow], CompressionCapsEnumeration, CompressionCaps_CanBFrame, CompressionCaps_CanCrunch, CompressionCaps_CanKeyFrame, CompressionCaps_CanQuality, CompressionCaps_CanWindow, dshow.compressioncaps, strmif/CompressionCaps, strmif/CompressionCaps_CanBFrame, strmif/CompressionCaps_CanCrunch, strmif/CompressionCaps_CanKeyFrame, strmif/CompressionCaps_CanQuality, strmif/CompressionCaps_CanWindow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - CompressionCaps
product: Windows
targetos: Windows
req.typenames: CompressionCaps
req.redist: 
---

# CompressionCaps enumeration


## -description



Indicates video compression capabilities.




## -enum-fields




### -field CompressionCaps_CanQuality

Video compressor supports the <a href="https://msdn.microsoft.com/7ecc00f9-73d4-4d26-b7b0-1b6419027d69">IAMVideoCompression::put_Quality</a> and <a href="https://msdn.microsoft.com/a34b6d15-3c84-476e-bd2f-ee10b59ded82">IAMVideoCompression::get_Quality</a> methods.


### -field CompressionCaps_CanCrunch

Video compressor can compress video to a specified data rate. If the compressor has this capability then the output pins media type will contain the data rate in the <a href="https://msdn.microsoft.com/a175592b-0dc1-4001-b52f-785407965932">VIDEOINFOHEADER</a> structure's <b>dwBitRate</b> member. The only way to set the data rate is to set <b>dwBitRate</b>.


### -field CompressionCaps_CanKeyFrame

Video compressor supports the <a href="https://msdn.microsoft.com/dc229333-3524-4228-ab13-a6e9619643fd">IAMVideoCompression::put_KeyFrameRate</a> and <a href="https://msdn.microsoft.com/af73cfaa-3297-44a7-96a7-8805aad057e2">IAMVideoCompression::get_KeyFrameRate</a> methods.


### -field CompressionCaps_CanBFrame

Video compressor supports the <a href="https://msdn.microsoft.com/bf1dfc28-a6c7-4c0d-96ea-8cf417b13a10">IAMVideoCompression::put_PFramesPerKeyFrame</a> and <a href="https://msdn.microsoft.com/621292dd-42d9-4458-8971-929db39ed8b9">IAMVideoCompression::get_PFramesPerKeyFrame</a> methods.


### -field CompressionCaps_CanWindow

Video compressor supports the <a href="https://msdn.microsoft.com/744cd32d-5f61-4069-82c4-50bc1b800f24">IAMVideoCompression::put_WindowSize</a> and <a href="https://msdn.microsoft.com/1f12aa72-3468-4dca-a5f6-43f64f6d2f83">IAMVideoCompression::get_WindowSize</a> methods.


## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/6b7d8a98-35b8-442f-bf51-9e66fd03e2c9">IAMVideoCompression Interface</a>
 

 

