---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorGetStreamPalette
title: ID3D11VideoContext::VideoProcessorGetStreamPalette (d3d11.h)
author: windows-sdk-content
description: Gets the color-palette entries for an input stream on the video processor.
old-location: mf\id3d11videocontext_videoprocessorgetstreampalette.htm
tech.root: medfound
ms.assetid: 009568EA-7230-42C0-B35F-AB0A1AF8EC2A
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorGetStreamPalette method, ID3D11VideoContext.VideoProcessorGetStreamPalette, ID3D11VideoContext::VideoProcessorGetStreamPalette, VideoProcessorGetStreamPalette, VideoProcessorGetStreamPalette method [Media Foundation], VideoProcessorGetStreamPalette method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorGetStreamPalette, mf.id3d11videocontext_videoprocessorgetstreampalette
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
 - ID3D11VideoContext.VideoProcessorGetStreamPalette
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext::VideoProcessorGetStreamPalette


## -description


Gets the color-palette entries for an input stream on the video processor.


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/5A5FB7F9-F299-4E67-AFAD-E7056CBAEE76">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="https://msdn.microsoft.com/BE213FFE-FB1D-4BDC-A1AA-2EA487DF8D4A">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.


### -param Count [in]

The number of entries in the <i>pEntries</i> array.


### -param pEntries [out]

A pointer to a <b>UINT</b> array allocated by the caller. The method fills the array with the palette entries. For RGB streams, the palette entries use the <b>DXGI_FORMAT_B8G8R8A8</b> representation. For YCbCr streams, the palette entries use the <b>DXGI_FORMAT_AYUV</b> representation.


## -returns



This method does not return a value.




## -remarks



This method applies only to input streams that have a palettized color format. Palettized formats with 4 bits per pixel (bpp) use 16 palette entries. Formats with 8 bpp use 256 entries.




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

