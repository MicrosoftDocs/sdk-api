---
UID: NF:msacm.acmStreamReset
title: acmStreamReset function (msacm.h)
description: The acmStreamReset function stops conversions for a given ACM stream. All pending buffers are marked as done and returned to the application.
helpviewer_keywords: ["_win32_acmStreamReset","acmStreamReset","acmStreamReset function [Windows Multimedia]","msacm/acmStreamReset","multimedia.acmstreamreset"]
old-location: multimedia\acmstreamreset.htm
tech.root: Multimedia
ms.assetid: 641c882e-b9c8-4945-bf8a-f3e70c5d5c64
ms.date: 12/05/2018
ms.keywords: _win32_acmStreamReset, acmStreamReset, acmStreamReset function [Windows Multimedia], msacm/acmStreamReset, multimedia.acmstreamreset
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
 - acmStreamReset
 - msacm/acmStreamReset
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
 - acmStreamReset
---

# acmStreamReset function


## -description

The <b>acmStreamReset</b> function stops conversions for a given ACM stream. All pending buffers are marked as done and returned to the application.

## -parameters

### -param has

Handle to the conversion stream.

### -param fdwReset

Reserved; must be zero.

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
</table>

## -remarks

Resetting an ACM conversion stream is necessary only for asynchronous conversion streams. Resetting a synchronous conversion stream will succeed, but no action will be taken.

## -see-also

<a href="/windows/desktop/Multimedia/audio-compression-functions">Audio Compression Functions</a>



<a href="/windows/desktop/Multimedia/audio-compression-manager">Audio Compression Manager</a>