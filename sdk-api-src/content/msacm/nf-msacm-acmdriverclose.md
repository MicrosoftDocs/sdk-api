---
UID: NF:msacm.acmDriverClose
title: acmDriverClose function (msacm.h)
description: The acmDriverClose function closes a previously opened ACM driver instance. If the function is successful, the handle is invalidated.
helpviewer_keywords: ["_win32_acmDriverClose","acmDriverClose","acmDriverClose function [Windows Multimedia]","msacm/acmDriverClose","multimedia.acmdriverclose"]
old-location: multimedia\acmdriverclose.htm
tech.root: Multimedia
ms.assetid: f756c11d-54a7-4238-8a99-4263a6c36109
ms.date: 12/05/2018
ms.keywords: _win32_acmDriverClose, acmDriverClose, acmDriverClose function [Windows Multimedia], msacm/acmDriverClose, multimedia.acmdriverclose
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
 - acmDriverClose
 - msacm/acmDriverClose
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
 - acmDriverClose
---

# acmDriverClose function


## -description

The <b>acmDriverClose</b> function closes a previously opened ACM driver instance. If the function is successful, the handle is invalidated.

## -parameters

### -param had

Handle to the open driver instance to be closed.

### -param fdwClose

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
<dt><b>ACMERR_BUSY</b></dt>
</dl>
</td>
<td width="60%">
The driver is in use and cannot be closed.

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
</table>

## -see-also

<a href="/windows/desktop/Multimedia/audio-compression-functions">Audio Compression Functions</a>



<a href="/windows/desktop/Multimedia/audio-compression-manager">Audio Compression Manager</a>