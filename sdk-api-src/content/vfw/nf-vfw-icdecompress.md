---
UID: NF:vfw.ICDecompress
title: ICDecompress function
author: windows-sdk-content
description: The ICDecompress function decompresses a single video frame.
old-location: multimedia\icdecompress.htm
old-project: Multimedia
ms.assetid: 779b63db-6b1d-4eb5-9df5-bb847b35863d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ICDecompress, ICDecompress function [Windows Multimedia], _win32_ICDecompress, multimedia.icdecompress, vfw/ICDecompress
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: VS_FIXEDFILEINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msvfw32.dll
api_name:
 - ICDecompress
product: Windows
targetos: Windows
req.lib: Vfw32.lib
req.dll: Msvfw32.dll
req.irql: 
req.product: Windows UI
---

# ICDecompress function


## -description



The <b>ICDecompress</b> function decompresses a single video frame.




## -parameters




### -param hic

Handle to the decompressor to use.
          


### -param dwFlags

Applicable decompression flags. The following values are defined.

<table>
<tr>
<th>Value
                </th>
<th>Meaning
                </th>
</tr>
<tr>
<td><b>ICDECOMPRESS_HURRYUP</b></td>
<td>Tries to decompress at a faster rate. When an application uses this flag, the driver should buffer the decompressed data but not draw the image.</td>
</tr>
<tr>
<td><b>ICDECOMPRESS_NOTKEYFRAME</b></td>
<td>Current frame is not a key frame.</td>
</tr>
<tr>
<td><b>ICDECOMPRESS_NULLFRAME</b></td>
<td>Current frame does not contain data and the decompressed image should be left the same.</td>
</tr>
<tr>
<td><b>ICDECOMPRESS_PREROLL</b></td>
<td>Current frame precedes the point in the movie where playback starts and, therefore, will not be drawn.</td>
</tr>
<tr>
<td><b>ICDECOMPRESS_UPDATE</b></td>
<td>Screen is being updated or refreshed.</td>
</tr>
</table>
 


### -param lpbiFormat

Pointer to a <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure containing the format of the compressed data.
          


### -param lpData

Pointer to the input data.
          


### -param lpbi

Pointer to a <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure containing the output format.
          


### -param lpBits

Pointer to a buffer that is large enough to contain the decompressed data.
          


## -returns



Returns ICERR_OK if successful or an error otherwise.
          




## -see-also




<a href="https://msdn.microsoft.com/193961a5-b882-4769-bce7-a53d625fc9dd">Video Compression Functions</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

