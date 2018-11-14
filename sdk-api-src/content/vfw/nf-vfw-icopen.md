---
UID: NF:vfw.ICOpen
title: ICOpen function
author: windows-sdk-content
description: The ICOpen function opens a compressor or decompressor.
old-location: multimedia\icopen.htm
tech.root: Multimedia
ms.assetid: 2637b6ef-2324-40db-99e4-773fcb6fdbf6
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: ICOpen, ICOpen function [Windows Multimedia], _win32_ICOpen, multimedia.icopen, vfw/ICOpen
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Vfw32.lib
req.dll: Msvfw32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msvfw32.dll
api_name:
 - ICOpen
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ICOpen
: 
---

# ICOpen function


## -description



The <b>ICOpen</b> function opens a compressor or decompressor.




## -parameters




### -param fccType

Four-character code indicating the type of compressor or decompressor to open. For video streams, the value of this parameter is "VIDC".


### -param fccHandler

Preferred handler of the specified type. Typically, the handler type is stored in the stream header in an AVI file.


### -param wMode

Flag defining the use of the compressor or decompressor. The following values are defined.

<table>
<tr>
<th>Value
                </th>
<th>Meaning
                </th>
</tr>
<tr>
<td>ICMODE_COMPRESS</td>
<td>Compressor will perform normal compression.</td>
</tr>
<tr>
<td>ICMODE_DECOMPRESS</td>
<td>Decompressor will perform normal decompression.</td>
</tr>
<tr>
<td>ICMODE_DRAW</td>
<td>Decompressor will decompress and draw the data directly to hardware.</td>
</tr>
<tr>
<td>ICMODE_FASTCOMPRESS</td>
<td>Compressor will perform fast (real-time) compression.</td>
</tr>
<tr>
<td>ICMODE_FASTDECOMPRESS</td>
<td>Decompressor will perform fast (real-time) decompression.</td>
</tr>
<tr>
<td>ICMODE_QUERY</td>
<td>Queries the compressor or decompressor for information.</td>
</tr>
</table>
 


## -returns



Returns a handle to a compressor or decompressor if successful or zero otherwise.




## -see-also




<a href="https://msdn.microsoft.com/193961a5-b882-4769-bce7-a53d625fc9dd">Video Compression Functions</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

