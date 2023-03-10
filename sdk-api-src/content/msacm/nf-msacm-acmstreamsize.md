---
UID: NF:msacm.acmStreamSize
title: acmStreamSize function (msacm.h)
description: The acmStreamSize function returns a recommended size for a source or destination buffer on an ACM stream.
helpviewer_keywords: ["_win32_acmStreamSize","acmStreamSize","acmStreamSize function [Windows Multimedia]","msacm/acmStreamSize","multimedia.acmstreamsize"]
old-location: multimedia\acmstreamsize.htm
tech.root: Multimedia
ms.assetid: 44b8c2cb-ae37-4919-83af-4a8ce6f8737c
ms.date: 12/05/2018
ms.keywords: _win32_acmStreamSize, acmStreamSize, acmStreamSize function [Windows Multimedia], msacm/acmStreamSize, multimedia.acmstreamsize
req.header: msacm.h
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
req.lib: Msacm32.lib
req.dll: Msacm32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - acmStreamSize
 - msacm/acmStreamSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msacm32.dll
 - Ext-MS-Win-mm-msacm-l1-1-0.dll
api_name:
 - acmStreamSize
---

# acmStreamSize function


## -description

The <b>acmStreamSize</b> function returns a recommended size for a source or destination buffer on an ACM stream.

## -parameters

### -param has

Handle to the conversion stream.

### -param cbInput

Size, in bytes, of the source or destination buffer. The <i>fdwSize</i> flags specify what the input parameter defines. This parameter must be nonzero.

### -param pdwOutputBytes

Pointer to a variable that contains the size, in bytes, of the source or destination buffer. The <i>fdwSize</i> flags specify what the output parameter defines. If the <b>acmStreamSize</b> function succeeds, this location will always be filled with a nonzero value.

### -param fdwSize

Flags for the stream size query. The following values are defined:

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td>ACM_STREAMSIZEF_DESTINATION</td>
<td>The <i>cbInput</i> parameter contains the size of the destination buffer. The <i>pdwOutputBytes</i> parameter will receive the recommended source buffer size, in bytes.</td>
</tr>
<tr>
<td>ACM_STREAMSIZEF_SOURCE</td>
<td>The <i>cbInput</i> parameter contains the size of the source buffer. The <i>pdwOutputBytes</i> parameter will receive the recommended destination buffer size, in bytes.</td>
</tr>
</table>

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
<dt><b>ACMERR_NOTPOSSIBLE</b></dt>
</dl>
</td>
<td width="60%">
The requested operation cannot be performed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALFLAG</b></dt>
</dl>
</td>
<td width="60%">
At least one flag is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALHANDLE</b></dt>
</dl>
</td>
<td width="60%">
The specified handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALPARAM</b></dt>
</dl>
</td>
<td width="60%">
At least one parameter is invalid.

</td>
</tr>
</table>

## -remarks

An application can use this function to determine suggested buffer sizes for either source or destination buffers. The buffer sizes returned might be only an estimation of the actual sizes required for conversion. Because actual conversion sizes cannot always be determined without performing the conversion, the sizes returned will usually be overestimated.

In the event of an error, the location pointed to by <i>pdwOutputBytes</i> will receive zero. This assumes that the pointer specified by <i>pdwOutputBytes</i> is valid.

## -see-also

<a href="/windows/desktop/Multimedia/audio-compression-functions">Audio Compression Functions</a>



<a href="/windows/desktop/Multimedia/audio-compression-manager">Audio Compression Manager</a>