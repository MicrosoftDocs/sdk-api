---
UID: NF:d3d11_1.ID3D11VideoContext1.VideoProcessorGetOutputColorSpace1
title: ID3D11VideoContext1::VideoProcessorGetOutputColorSpace1
author: windows-sdk-content
description: Gets the color space information for the video processor output surface.
old-location: mf\id3d11videocontext1_videoprocessorgetoutputcolorspace1.htm
tech.root: medfound
ms.assetid: 1B2BC801-CC5C-460C-A10E-CCDEE35A8E27
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: ID3D11VideoContext1 interface [Media Foundation],VideoProcessorGetOutputColorSpace1 method, ID3D11VideoContext1.VideoProcessorGetOutputColorSpace1, ID3D11VideoContext1::VideoProcessorGetOutputColorSpace1, VideoProcessorGetOutputColorSpace1, VideoProcessorGetOutputColorSpace1 method [Media Foundation], VideoProcessorGetOutputColorSpace1 method [Media Foundation],ID3D11VideoContext1 interface, d3d11_1/ID3D11VideoContext1::VideoProcessorGetOutputColorSpace1, mf.id3d11videocontext1_videoprocessorgetoutputcolorspace1
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - COM
api_location:
 - d3d11_1.h
api_name:
 - ID3D11VideoContext1.VideoProcessorGetOutputColorSpace1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext1::VideoProcessorGetOutputColorSpace1


## -description


Gets the color space information for the video processor output surface.


## -parameters




### -param pVideoProcessor [in]

Type: <b>ID3D11VideoProcessor*</b>

A pointer to the <a href="https://msdn.microsoft.com/en-us/library/Hh447799(v=VS.85).aspx">ID3D11VideoProcessor</a> interface.


### -param pColorSpace [out]

Type: <b>DXGI_COLOR_SPACE_TYPE*</b>

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/Dn903661(v=VS.85).aspx">DXGI_COLOR_SPACE_TYPE</a> value that indicates the colorspace for the video processor output surface.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn894126(v=VS.85).aspx">ID3D11VideoContext1</a>
 

 

