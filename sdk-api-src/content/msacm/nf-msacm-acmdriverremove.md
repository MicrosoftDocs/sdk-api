---
UID: NF:msacm.acmDriverRemove
title: acmDriverRemove function (msacm.h)
description: The acmDriverRemove function removes an ACM driver from the list of available ACM drivers. The driver will be removed for the calling application only. If the driver is globally installed, other applications will still be able to use it.
helpviewer_keywords: ["_win32_acmDriverRemove","acmDriverRemove","acmDriverRemove function [Windows Multimedia]","msacm/acmDriverRemove","multimedia.acmdriverremove"]
old-location: multimedia\acmdriverremove.htm
tech.root: Multimedia
ms.assetid: 7182d452-a935-4ed5-808a-595fca4f0429
ms.date: 12/05/2018
ms.keywords: _win32_acmDriverRemove, acmDriverRemove, acmDriverRemove function [Windows Multimedia], msacm/acmDriverRemove, multimedia.acmdriverremove
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
 - acmDriverRemove
 - msacm/acmDriverRemove
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
 - acmDriverRemove
---

# acmDriverRemove function


## -description

The <b>acmDriverRemove</b> function removes an ACM driver from the list of available ACM drivers. The driver will be removed for the calling application only. If the driver is globally installed, other applications will still be able to use it.

## -parameters

### -param hadid

Handle to the driver identifier to be removed.

### -param fdwRemove

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
The driver is in use and cannot be removed.

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