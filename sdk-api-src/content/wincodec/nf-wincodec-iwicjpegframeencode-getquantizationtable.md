---
UID: NF:wincodec.IWICJpegFrameEncode.GetQuantizationTable
title: IWICJpegFrameEncode::GetQuantizationTable
author: windows-sdk-content
description: Retrieves a copy of the quantization table.
old-location: wic\iwicjpegframeencode_getquantizationtable.htm
tech.root: wic
ms.assetid: 6FBDAEA2-78E6-4152-815D-FA6164FE396F
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetQuantizationTable, GetQuantizationTable method [Windows Imaging Component], GetQuantizationTable method [Windows Imaging Component],IWICJpegFrameEncode interface, IWICJpegFrameEncode interface [Windows Imaging Component],GetQuantizationTable method, IWICJpegFrameEncode.GetQuantizationTable, IWICJpegFrameEncode::GetQuantizationTable, wic.iwicjpegframeencode_getquantizationtable, wincodec/IWICJpegFrameEncode::GetQuantizationTable
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
 - IWICJpegFrameEncode.GetQuantizationTable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICJpegFrameEncode::GetQuantizationTable


## -description


Retrieves a copy of the quantization table.


## -parameters




### -param scanIndex

Type: <b>UINT</b>

The zero-based index of the scan for which data is retrieved.


### -param tableIndex

Type: <b>UINT</b>

The index of the quantization table to retrieve. 


### -param pQuantizationTable [out]

Type: <b><a href="https://msdn.microsoft.com/DE1AAB15-B0B8-4594-BBCE-5F8EE5CE0AF7">DXGI_JPEG_QUANTIZATION_TABLE</a>*</b>

A pointer that receives the table data. This parameter must not be NULL.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method can return one of these values.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_OK</dt>
</dl>
</td>
<td width="60%">
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>WINCODEC_ERR_INVALIDJPEGSCANINDEX </dt>
</dl>
</td>
<td width="60%">
The specified scan index is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>WINCODEC_ERR_INVALIDPARAMETER</dt>
</dl>
</td>
<td width="60%">
Can occur if <i>pTable</i> is NULL or if <i>tableIndex</i> does not point to a valid table slot. Check the scan header for valid table indices.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/631571A2-AA15-4A4B-B705-6CCC81392A6A">IWICJpegFrameEncode</a>
 

 

