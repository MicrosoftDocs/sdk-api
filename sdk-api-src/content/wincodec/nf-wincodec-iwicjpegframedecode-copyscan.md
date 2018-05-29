---
UID: NF:wincodec.IWICJpegFrameDecode.CopyScan
title: IWICJpegFrameDecode::CopyScan
author: windows-sdk-content
description: Retrieves a copy of the compressed JPEG scan directly from the WIC decoder frame's output stream.
old-location: wic\iwicjpegframedecode_copyscan.htm
old-project: wic
ms.assetid: 19579C0B-AB96-424D-B433-6A88BE64A434
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: CopyScan, CopyScan method [Windows Imaging Component], CopyScan method [Windows Imaging Component],IWICJpegFrameDecode interface, IWICJpegFrameDecode interface [Windows Imaging Component],CopyScan method, IWICJpegFrameDecode.CopyScan, IWICJpegFrameDecode::CopyScan, wic.iwicjpegframedecode_copyscan, wincodec/IWICJpegFrameDecode::CopyScan
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: WICTiffCompressionOption
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.dll
api_name:
-	IWICJpegFrameDecode.CopyScan
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICJpegFrameDecode::CopyScan


## -description


Retrieves a copy of the compressed JPEG scan directly from the WIC decoder frame's output stream.


## -parameters




### -param scanIndex

Type: <b>UINT</b>

The zero-based index of the scan for which data is retrieved.


### -param scanOffset

Type: <b>UINT</b>

The byte position in the scan data to begin copying.  Use 0 on the first call.  If the output buffer size is insufficient to store the entire scan, this offset allows you to resume copying from the end of the previous copy operation.


### -param cbScanData

Type: <b>UINT</b>

The size, in bytes, of the <i>pbScanData</i> array.


### -param pbScanData [out]

Type: <b>BYTE*</b>

A pointer that receives the table data. This parameter must not be NULL.


### -param pcbScanDataActual [out]

Type: <b>UINT*</b>

A pointer that receives the size of the scan data actually copied into <i>pbScanData</i>. The size returned may be smaller that the size of <i>cbScanData</i>. This  parameter may be NULL.


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/E6310320-53A8-40F1-8964-D21D8054E1B8">IWICJpegFrameDecode</a>
 

 

