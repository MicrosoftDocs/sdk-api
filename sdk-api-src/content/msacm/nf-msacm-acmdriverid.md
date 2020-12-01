---
UID: NF:msacm.acmDriverID
title: acmDriverID function (msacm.h)
description: The acmDriverID function returns the handle of an ACM driver identifier associated with an open ACM driver instance or stream handle.
helpviewer_keywords: ["_win32_acmDriverID","acmDriverID","acmDriverID function [Windows Multimedia]","msacm/acmDriverID","multimedia.acmdriverid"]
old-location: multimedia\acmdriverid.htm
tech.root: Multimedia
ms.assetid: d88ec472-80b7-4563-a09d-65e0e829c14e
ms.date: 12/05/2018
ms.keywords: _win32_acmDriverID, acmDriverID, acmDriverID function [Windows Multimedia], msacm/acmDriverID, multimedia.acmdriverid
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
 - acmDriverID
 - msacm/acmDriverID
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
 - acmDriverID
---

# acmDriverID function


## -description

The <b>acmDriverID</b> function returns the handle of an ACM driver identifier associated with an open ACM driver instance or stream handle.

## -parameters

### -param hao

Handle to the open driver instance or stream handle. This is the handle of an ACM object, such as <b>HACMDRIVER</b> or <b>HACMSTREAM</b>.

### -param phadid

Pointer to a buffer that receives a handle identifying the installed driver that is associated with <i>hao</i>.

### -param fdwDriverID

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

## -see-also

<a href="/windows/desktop/Multimedia/audio-compression-functions">Audio Compression Functions</a>



<a href="/windows/desktop/Multimedia/audio-compression-manager">Audio Compression Manager</a>