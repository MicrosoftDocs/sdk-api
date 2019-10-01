---
UID: NF:wincodec.IWICJpegFrameEncode.WriteScan
title: IWICJpegFrameEncode::WriteScan (wincodec.h)
author: windows-sdk-content
description: Writes scan data to a JPEG frame.
old-location: wic\iwicjpegframeencode_writescan.htm
tech.root: wic
ms.assetid: FED02403-E696-4988-BFB6-F1E37D9FA5F1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWICJpegFrameEncode interface [Windows Imaging Component],WriteScan method, IWICJpegFrameEncode.WriteScan, IWICJpegFrameEncode::WriteScan, WriteScan, WriteScan method [Windows Imaging Component], WriteScan method [Windows Imaging Component],IWICJpegFrameEncode interface, wic.iwicjpegframeencode_writescan, wincodec/IWICJpegFrameEncode::WriteScan
ms.topic: method
f1_keywords: 
 - "wincodec/IWICJpegFrameEncode.WriteScan"
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICJpegFrameEncode.WriteScan
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICJpegFrameEncode::WriteScan


## -description


Writes scan data to a JPEG frame.


## -parameters




### -param cbScanData

Type: <b>UINT</b>

The size of the data in the <i>pbScanData</i> parameter.


### -param pbScanData

Type: <b>BYTE*</b>

The scan data to write.


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

Returns S_OK on successful completion.




## -remarks



<b>WriteScan</b> may be called multiple times.  Each call appends the scan data specified to any previous scan data.  Complete the scan by calling <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-commit">IWICBitmapFrameEncode::Commit</a>.



Any calls to set encoder parameters or image metadata that will appear before the scan data in the resulting JPEG file must be completed before the first call to this method.  This includes calls to <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts">IWICBitmapFrameEncode::SetColorContexts</a> , <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-setpalette">IWICBitmapFrameEncode::SetPalette</a>, <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat">IWICBitmapFrameEncode::SetPixelFormat</a>, <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-setresolution">IWICBitmapFrameEncode::SetResolution</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail">IWICBitmapFrameEncode::SetThumbnail</a>.  <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-setsize">IWICBitmapFrameEncode::SetSize</a> is required as it has no default value for encoded image size.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframeencode">IWICBitmapFrameEncode</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicjpegframeencode">IWICJpegFrameEncode</a>
 

 

