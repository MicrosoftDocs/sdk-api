---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorSetStreamPalette
title: ID3D11VideoContext::VideoProcessorSetStreamPalette
author: windows-sdk-content
description: Sets the color-palette entries for an input stream on the video processor.
old-location: mf\id3d11videocontext_videoprocessorsetstreampalette.htm
tech.root: medfound
ms.assetid: E2816D5F-0541-45B0-A90A-7C26530D064C
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorSetStreamPalette method, ID3D11VideoContext.VideoProcessorSetStreamPalette, ID3D11VideoContext::VideoProcessorSetStreamPalette, VideoProcessorSetStreamPalette, VideoProcessorSetStreamPalette method [Media Foundation], VideoProcessorSetStreamPalette method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorSetStreamPalette, mf.id3d11videocontext_videoprocessorsetstreampalette
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.h
api_name:
 - ID3D11VideoContext.VideoProcessorSetStreamPalette
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext::VideoProcessorSetStreamPalette


## -description


Sets the color-palette entries for an input stream on the video processor.


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/5A5FB7F9-F299-4E67-AFAD-E7056CBAEE76">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="https://msdn.microsoft.com/BE213FFE-FB1D-4BDC-A1AA-2EA487DF8D4A">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.


### -param Count [in]

The number of elements in the <i>pEntries</i> array.


### -param pEntries [in]

A pointer to an array of palette entries. For RGB streams, the palette entries use the <b>DXGI_FORMAT_B8G8R8A8</b> representation. For YCbCr streams, the palette entries use the <b>DXGI_FORMAT_AYUV</b> representation. The caller allocates the array.


## -returns



This method does not return a value.




## -remarks



This method applies only to  input streams that have a palettized color format. Palettized formats with 4 bits per pixel (bpp) use the first 16 entries in the list. Formats with 8 bpp use the first 256 entries.

If a pixel has a palette index greater than the number of entries, the device treats the pixel as white with opaque alpha. For full-range RGB, this value is (255, 255, 255, 255); for YCbCr the value is (255, 235, 128, 128).

If the driver does not report the <b>D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_ALPHA_PALETTE</b> capability flag, every palette entry must have an alpha value of 0xFF (opaque). To query for this capability, call <a href="https://msdn.microsoft.com/BE213FFE-FB1D-4BDC-A1AA-2EA487DF8D4A">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a>.




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

