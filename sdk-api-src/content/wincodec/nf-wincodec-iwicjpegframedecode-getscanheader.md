---
UID: NF:wincodec.IWICJpegFrameDecode.GetScanHeader
title: IWICJpegFrameDecode::GetScanHeader
author: windows-sdk-content
description: Retrieves parameters from the Start Of Scan (SOS) marker for the scan with the specified index.
old-location: wic\iwicjpegframedecode_getscanheader.htm
tech.root: wic
ms.assetid: FD434498-CC04-4702-ACD3-EDD1DDE0B3AA
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetScanHeader, GetScanHeader method [Windows Imaging Component], GetScanHeader method [Windows Imaging Component],IWICJpegFrameDecode interface, IWICJpegFrameDecode interface [Windows Imaging Component],GetScanHeader method, IWICJpegFrameDecode.GetScanHeader, IWICJpegFrameDecode::GetScanHeader, wic.iwicjpegframedecode_getscanheader, wincodec/IWICJpegFrameDecode::GetScanHeader
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IWICJpegFrameDecode.GetScanHeader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wincodec.h
: 
- IWICJpegFrameDecode.GetScanHeader
: 
---

# IWICJpegFrameDecode::GetScanHeader


## -description


Retrieves parameters from the Start Of Scan (SOS) marker for the scan with the specified index.


## -parameters




### -param scanIndex

Type: <b>UINT</b>

The index of the scan for which header data is retrieved.


### -param pScanHeader [out]

Type: <b><a href="https://msdn.microsoft.com/87A36F9B-CD6B-4343-AAA7-9FDBAD41E38A">WICJpegScanHeader</a>*</b>

A pointer that receives the frame header data.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns S_OK on successful completion.




## -see-also




<a href="https://msdn.microsoft.com/E6310320-53A8-40F1-8964-D21D8054E1B8">IWICJpegFrameDecode</a>
 

 

