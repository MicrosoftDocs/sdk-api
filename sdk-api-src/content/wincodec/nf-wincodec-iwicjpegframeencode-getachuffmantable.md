---
UID: NF:wincodec.IWICJpegFrameEncode.GetAcHuffmanTable
title: IWICJpegFrameEncode::GetAcHuffmanTable
author: windows-sdk-content
description: Retrieves a copy of the AC Huffman table for the specified scan and table.
old-location: wic\iwicjpegframeencode_getachuffmantable.htm
tech.root: wic
ms.assetid: 9ABE4C1E-52C7-4F08-8479-CB4F6FEE9ADA
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetAcHuffmanTable, GetAcHuffmanTable method [Windows Imaging Component], GetAcHuffmanTable method [Windows Imaging Component],IWICJpegFrameEncode interface, IWICJpegFrameEncode interface [Windows Imaging Component],GetAcHuffmanTable method, IWICJpegFrameEncode.GetAcHuffmanTable, IWICJpegFrameEncode::GetAcHuffmanTable, wic.iwicjpegframeencode_getachuffmantable, wincodec/IWICJpegFrameEncode::GetAcHuffmanTable
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
 - IWICJpegFrameEncode.GetAcHuffmanTable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICJpegFrameEncode::GetAcHuffmanTable


## -description


Retrieves a copy of the AC Huffman table for the specified scan and table.


## -parameters




### -param scanIndex

Type: <b>UINT</b>

The zero-based index of the scan for which data is retrieved.


### -param tableIndex

Type: <b>UINT</b>

The index of the AC Huffman table to retrieve.


### -param pAcHuffmanTable [out]

Type: <b><a href="https://msdn.microsoft.com/E1923FFA-E7E5-4158-9793-3E7F5A6EA7FA">DXGI_JPEG_AC_HUFFMAN_TABLE</a>*</b>

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
Can occur if <i>pAcHuffmanTable</i> is NULL or if <i>tableIndex</i> does not point to a valid table slot. Check the scan header for valid table indices.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/631571A2-AA15-4A4B-B705-6CCC81392A6A">IWICJpegFrameEncode</a>
 

 

