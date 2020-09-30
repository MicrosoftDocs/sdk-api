---
UID: NF:wincodec.IWICJpegFrameDecode.GetFrameHeader
title: IWICJpegFrameDecode::GetFrameHeader (wincodec.h)
description: Retrieves header data from the entire frame.
helpviewer_keywords: ["GetFrameHeader","GetFrameHeader method [Windows Imaging Component]","GetFrameHeader method [Windows Imaging Component]","IWICJpegFrameDecode interface","IWICJpegFrameDecode interface [Windows Imaging Component]","GetFrameHeader method","IWICJpegFrameDecode.GetFrameHeader","IWICJpegFrameDecode::GetFrameHeader","wic.iwicjpegframedecode_getframeheader","wincodec/IWICJpegFrameDecode::GetFrameHeader"]
old-location: wic\iwicjpegframedecode_getframeheader.htm
tech.root: wic
ms.assetid: CE29251F-C2E2-422B-B6BD-034D6B479009
ms.date: 12/05/2018
ms.keywords: GetFrameHeader, GetFrameHeader method [Windows Imaging Component], GetFrameHeader method [Windows Imaging Component],IWICJpegFrameDecode interface, IWICJpegFrameDecode interface [Windows Imaging Component],GetFrameHeader method, IWICJpegFrameDecode.GetFrameHeader, IWICJpegFrameDecode::GetFrameHeader, wic.iwicjpegframedecode_getframeheader, wincodec/IWICJpegFrameDecode::GetFrameHeader
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICJpegFrameDecode::GetFrameHeader
 - wincodec/IWICJpegFrameDecode::GetFrameHeader
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICJpegFrameDecode.GetFrameHeader
---

# IWICJpegFrameDecode::GetFrameHeader


## -description

Retrieves  header data from the entire frame.  The result includes parameters from the Start Of Frame (SOF) marker for the scan as well as parameters derived from other metadata such as the color model of the compressed data.

## -parameters

### -param pFrameHeader [out]

Type: <b><a href="/windows/desktop/api/wincodec/ns-wincodec-wicjpegframeheader">WICJpegFrameHeader</a>*</b>

A pointer that receives the frame header data.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK on successful completion.

## -see-also

<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicjpegframedecode">IWICJpegFrameDecode</a>



<a href="/windows/desktop/api/wincodec/ns-wincodec-wicjpegframeheader">WICJpegFrameHeader</a>