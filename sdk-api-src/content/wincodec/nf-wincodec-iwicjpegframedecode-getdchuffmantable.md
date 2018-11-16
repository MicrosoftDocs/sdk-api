---
UID: NF:wincodec.IWICJpegFrameDecode.GetDcHuffmanTable
title: IWICJpegFrameDecode::GetDcHuffmanTable
author: windows-sdk-content
description: Retrieves a copy of the DC Huffman table for the specified scan and table.
old-location: wic\iwicjpegframedecode_getdchuffmantable.htm
tech.root: wic
ms.assetid: 3C4FAF86-87CD-4844-94BC-CEE861681760
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetDcHuffmanTable, GetDcHuffmanTable method [Windows Imaging Component], GetDcHuffmanTable method [Windows Imaging Component],IWICJpegFrameDecode interface, IWICJpegFrameDecode interface [Windows Imaging Component],GetDcHuffmanTable method, IWICJpegFrameDecode.GetDcHuffmanTable, IWICJpegFrameDecode::GetDcHuffmanTable, wic.iwicjpegframedecode_getdchuffmantable, wincodec/IWICJpegFrameDecode::GetDcHuffmanTable
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
 - IWICJpegFrameDecode.GetDcHuffmanTable
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
- IWICJpegFrameDecode.GetDcHuffmanTable
: 
---

# IWICJpegFrameDecode::GetDcHuffmanTable


## -description


Retrieves a copy of the DC Huffman table for the specified scan and table.


## -parameters




### -param scanIndex

Type: <b>UINT</b>

The zero-based index of the scan for which data is retrieved.


### -param tableIndex

Type: <b>UINT</b>

The index of the DC Huffman table to retrieve. Valid indices for a given scan can be determined by retrieving the scan header with <a href="https://msdn.microsoft.com/FD434498-CC04-4702-ACD3-EDD1DDE0B3AA">IWICJpegFrameDecode::GetScanHeader</a>.


### -param pDcHuffmanTable [out]

Type: <b><a href="https://msdn.microsoft.com/E1923FFA-E7E5-4158-9793-3E7F5A6EA7FA">DXGI_JPEG_AC_HUFFMAN_TABLE</a>*</b>

A pointer that receives the table data. This parameter must not be NULL.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

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




<a href="https://msdn.microsoft.com/E6310320-53A8-40F1-8964-D21D8054E1B8">IWICJpegFrameDecode</a>
 

 

