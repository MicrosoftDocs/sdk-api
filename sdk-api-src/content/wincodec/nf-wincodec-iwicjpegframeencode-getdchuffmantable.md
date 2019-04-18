---
UID: NF:wincodec.IWICJpegFrameEncode.GetDcHuffmanTable
title: IWICJpegFrameEncode::GetDcHuffmanTable (wincodec.h)
author: windows-sdk-content
description: Retrieves a copy of the DC Huffman table for the specified scan and table.
old-location: wic\iwicjpegframeencode_getdchuffmantable.htm
tech.root: wic
ms.assetid: 8ACEFFBD-2F58-427D-8DB9-907A088A127B
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetDcHuffmanTable, GetDcHuffmanTable method [Windows Imaging Component], GetDcHuffmanTable method [Windows Imaging Component],IWICJpegFrameEncode interface, IWICJpegFrameEncode interface [Windows Imaging Component],GetDcHuffmanTable method, IWICJpegFrameEncode.GetDcHuffmanTable, IWICJpegFrameEncode::GetDcHuffmanTable, wic.iwicjpegframeencode_getdchuffmantable, wincodec/IWICJpegFrameEncode::GetDcHuffmanTable
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
 - IWICJpegFrameEncode.GetDcHuffmanTable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICJpegFrameEncode::GetDcHuffmanTable


## -description


Retrieves a copy of the DC Huffman table for the specified scan and table.


## -parameters




### -param scanIndex

The zero-based index of the scan for which data is retrieved.


### -param tableIndex

The index of the DC Huffman table to retrieve. 


### -param pDcHuffmanTable [out]

A pointer that receives the table data. This parameter must not be NULL.


## -returns



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
 

 

