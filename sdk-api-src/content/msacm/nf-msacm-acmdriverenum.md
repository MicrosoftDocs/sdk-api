---
UID: NF:msacm.acmDriverEnum
title: acmDriverEnum function (msacm.h)
description: The acmDriverEnum function enumerates the available ACM drivers, continuing until there are no more drivers or the callback function returns FALSE.
helpviewer_keywords: ["_win32_acmDriverEnum","acmDriverEnum","acmDriverEnum function [Windows Multimedia]","msacm/acmDriverEnum","multimedia.acmdriverenum"]
old-location: multimedia\acmdriverenum.htm
tech.root: Multimedia
ms.assetid: 3e93284d-2810-4c8e-9619-1989d8bf788e
ms.date: 12/05/2018
ms.keywords: _win32_acmDriverEnum, acmDriverEnum, acmDriverEnum function [Windows Multimedia], msacm/acmDriverEnum, multimedia.acmdriverenum
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
 - acmDriverEnum
 - msacm/acmDriverEnum
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
 - acmDriverEnum
---

# acmDriverEnum function


## -description

The <b>acmDriverEnum</b> function enumerates the available ACM drivers, continuing until there are no more drivers or the callback function returns <b>FALSE</b>.

## -parameters

### -param fnCallback

Procedure instance address of the application-defined callback function.

### -param dwInstance

A 64-bit (DWORD_PTR) or 32-bit (DWORD) application-defined value that is passed to the callback function along with ACM driver information.

### -param fdwEnum

Flags for enumerating ACM drivers. The following values are defined.

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td>ACM_DRIVERENUMF_DISABLED</td>
<td>Disabled ACM drivers should be included in the enumeration. Drivers can be disabled by the user through the Control Panel or by an application using the <a href="/windows/desktop/api/msacm/nf-msacm-acmdriverpriority">acmDriverPriority</a> function. If a driver is disabled, the <i>fdwSupport</i> parameter to the callback function will have the ACMDRIVERDETAILS_SUPPORTF_DISABLED flag set.</td>
</tr>
<tr>
<td>ACM_DRIVERENUMF_NOLOCAL</td>
<td>Only global drivers should be included in the enumeration.</td>
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
<dt><b>MMSYSERR_INVALPARAM</b></dt>
</dl>
</td>
<td width="60%">
At least one parameter is invalid.

</td>
</tr>
</table>

## -remarks

The <b>acmDriverEnum</b> function will return MMSYSERR_NOERROR (zero) if no ACM drivers are installed. Moreover, the callback function will not be called.

## -see-also

<a href="/windows/desktop/Multimedia/audio-compression-functions">Audio Compression Functions</a>



<a href="/windows/desktop/Multimedia/audio-compression-manager">Audio Compression Manager</a>