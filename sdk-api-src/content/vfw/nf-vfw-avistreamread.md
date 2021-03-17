---
UID: NF:vfw.AVIStreamRead
title: AVIStreamRead function (vfw.h)
description: The AVIStreamRead function reads audio, video or other data from a stream according to the stream type.
helpviewer_keywords: ["AVIStreamRead","AVIStreamRead function [Windows Multimedia]","_win32_AVIStreamRead","multimedia.avistreamread","vfw/AVIStreamRead"]
old-location: multimedia\avistreamread.htm
tech.root: Multimedia
ms.assetid: 9490d46f-b11d-466b-a756-092df2db0306
ms.date: 12/05/2018
ms.keywords: AVIStreamRead, AVIStreamRead function [Windows Multimedia], _win32_AVIStreamRead, multimedia.avistreamread, vfw/AVIStreamRead
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
 - AVIStreamRead
 - vfw/AVIStreamRead
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Avifil32.dll
 - Ext-MS-Win-Media-Avi-L1-1-0.dll
api_name:
 - AVIStreamRead
---

# AVIStreamRead function


## -description

The <b>AVIStreamRead</b> function reads audio, video or other data from a stream according to the stream type.

## -parameters

### -param pavi

Handle to an open stream.

### -param lStart

First sample to read.

### -param lSamples

Number of samples to read. You can also specify the value AVISTREAMREAD_CONVENIENT to let the stream handler determine the number of samples to read.

### -param lpBuffer

Pointer to a buffer to contain the data.

### -param cbBuffer

Size, in bytes, of the buffer pointed to by <i>lpBuffer</i>.

### -param plBytes

Pointer to a buffer that receives the number of bytes of data written in the buffer referenced by <i>lpBuffer</i>. This value can be <b>NULL</b>.

### -param plSamples

Pointer to a buffer that receives the number of samples written in the buffer referenced by <i>lpBuffer</i>. This value can be <b>NULL</b>.

## -returns

Returns zero if successful or an error otherwise. Possible error values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AVIERR_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The buffer size <i>cbBuffer</i> was smaller than a single sample of data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AVIERR_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was not enough memory to complete the read operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AVIERR_FILEREAD</b></dt>
</dl>
</td>
<td width="60%">
A disk error occurred while reading the file.

</td>
</tr>
</table>

## -remarks

If <i>lpBuffer</i> is <b>NULL</b>, this function does not read any data; it returns information about the size of data that would be read.

The argument <i>pavi</i> is a pointer to an <a href="/windows/desktop/api/vfw/nn-vfw-iavistream">IAVIStream</a> interface.

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>