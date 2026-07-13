---
UID: NF:vfw.AVIStreamWrite
title: AVIStreamWrite function (vfw.h)
description: The AVIStreamWrite function writes data to a stream.
helpviewer_keywords: ["AVIIF_KEYFRAME","AVIStreamWrite","AVIStreamWrite function [Windows Multimedia]","_win32_AVIStreamWrite","multimedia.avistreamwrite","vfw/AVIStreamWrite"]
old-location: multimedia\avistreamwrite.htm
tech.root: Multimedia
ms.assetid: 9a306939-7b4f-4e0b-8340-270725da74c3
ms.date: 12/05/2018
ms.keywords: AVIIF_KEYFRAME, AVIStreamWrite, AVIStreamWrite function [Windows Multimedia], _win32_AVIStreamWrite, multimedia.avistreamwrite, vfw/AVIStreamWrite
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
req.dll: Avifil32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AVIStreamWrite
 - vfw/AVIStreamWrite
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-media-avi-l1-1-0.dll
 - Avifil32.dll
api_name:
 - AVIStreamWrite
---

# AVIStreamWrite function


## -description

The <b>AVIStreamWrite</b> function writes data to a stream.

## -parameters

### -param pavi

Handle to an open stream.

### -param lStart

First sample to write.

### -param lSamples

Number of samples to write.

### -param lpBuffer

Pointer to a buffer containing the data to write.

### -param cbBuffer

Size of the buffer referenced by <i>lpBuffer</i>.

### -param dwFlags

Flag associated with this data. The following flag is defined:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AVIIF_KEYFRAME"></a><a id="aviif_keyframe"></a><dl>
<dt><b>AVIIF_KEYFRAME</b></dt>
</dl>
</td>
<td width="60%">
Indicates this data does not rely on preceding data in the file.

</td>
</tr>
</table>

### -param plSampWritten

Pointer to a buffer that receives the number of samples written. This can be set to <b>NULL</b>.

### -param plBytesWritten

Pointer to a buffer that receives the number of bytes written. This can be set to <b>NULL</b>.

## -returns

Returns zero if successful or an error otherwise.

## -remarks

The default AVI file handler supports writing only at the end of a stream. The "WAVE" file handler supports writing anywhere.

This function overwrites existing data, rather than inserting new data.

The argument <i>pavi</i> is a pointer to an <a href="/windows/desktop/api/vfw/nn-vfw-iavistream">IAVIStream</a> interface.

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>