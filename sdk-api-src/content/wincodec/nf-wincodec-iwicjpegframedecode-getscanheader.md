---
UID: NF:wincodec.IWICJpegFrameDecode.GetScanHeader
title: IWICJpegFrameDecode::GetScanHeader (wincodec.h)
description: Retrieves parameters from the Start Of Scan (SOS) marker for the scan with the specified index.
helpviewer_keywords: ["GetScanHeader","GetScanHeader method [Windows Imaging Component]","GetScanHeader method [Windows Imaging Component]","IWICJpegFrameDecode interface","IWICJpegFrameDecode interface [Windows Imaging Component]","GetScanHeader method","IWICJpegFrameDecode.GetScanHeader","IWICJpegFrameDecode::GetScanHeader","wic.iwicjpegframedecode_getscanheader","wincodec/IWICJpegFrameDecode::GetScanHeader"]
old-location: wic\iwicjpegframedecode_getscanheader.htm
tech.root: wic
ms.assetid: FD434498-CC04-4702-ACD3-EDD1DDE0B3AA
ms.date: 12/05/2018
ms.keywords: GetScanHeader, GetScanHeader method [Windows Imaging Component], GetScanHeader method [Windows Imaging Component],IWICJpegFrameDecode interface, IWICJpegFrameDecode interface [Windows Imaging Component],GetScanHeader method, IWICJpegFrameDecode.GetScanHeader, IWICJpegFrameDecode::GetScanHeader, wic.iwicjpegframedecode_getscanheader, wincodec/IWICJpegFrameDecode::GetScanHeader
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
 - IWICJpegFrameDecode::GetScanHeader
 - wincodec/IWICJpegFrameDecode::GetScanHeader
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
 - IWICJpegFrameDecode.GetScanHeader
---

# IWICJpegFrameDecode::GetScanHeader


## -description

Retrieves parameters from the Start Of Scan (SOS) marker for the scan with the specified index.

## -parameters

### -param scanIndex

Type: <b>UINT</b>

The index of the scan for which header data is retrieved.

### -param pScanHeader [out]

Type: <b><a href="/windows/desktop/api/wincodec/ns-wincodec-wicjpegscanheader">WICJpegScanHeader</a>*</b>

A pointer that receives the frame header data.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK on successful completion.

## -see-also

<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicjpegframedecode">IWICJpegFrameDecode</a>