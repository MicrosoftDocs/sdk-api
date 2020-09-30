---
UID: NC:msacm.ACMDRIVERENUMCB
title: ACMDRIVERENUMCB (msacm.h)
description: The acmDriverEnumCallback function specifies a callback function used with the acmDriverEnum function. The acmDriverEnumCallback name is a placeholder for an application-defined function name.
helpviewer_keywords: ["ACMDRIVERENUMCB","ACMDRIVERENUMCB callback","ACMDRIVERENUMCB callback function [Windows Multimedia]","_win32_acmDriverEnumCallback","acmDriverEnumCallback","msacm/ACMDRIVERENUMCB","multimedia.acmdriverenumcallback"]
old-location: multimedia\acmdriverenumcallback.htm
tech.root: Multimedia
ms.assetid: 8566fd31-ec0c-4325-b182-4765e81c7884
ms.date: 12/05/2018
ms.keywords: ACMDRIVERENUMCB, ACMDRIVERENUMCB callback, ACMDRIVERENUMCB callback function [Windows Multimedia], _win32_acmDriverEnumCallback, acmDriverEnumCallback, msacm/ACMDRIVERENUMCB, multimedia.acmdriverenumcallback
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ACMDRIVERENUMCB
 - msacm/ACMDRIVERENUMCB
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Msacm.h
api_name:
 - ACMDRIVERENUMCB
---

# ACMDRIVERENUMCB callback function


## -description

The <b>acmDriverEnumCallback</b> function specifies a callback function used with the <a href="/windows/desktop/api/msacm/nf-msacm-acmdriverenum">acmDriverEnum</a> function. The <b>acmDriverEnumCallback</b> name is a placeholder for an application-defined function name.

## -parameters

### -param hadid

Handle to an ACM driver identifier.

### -param dwInstance

Application-defined value specified in <a href="/windows/desktop/api/msacm/nf-msacm-acmdriverenum">acmDriverEnum</a>.

### -param fdwSupport

Driver-support flags specific to the driver specified by [ACMDRIVERDETAILS](./nf-msacm-acmdriverdetails.md) structure. This parameter can be a combination of the following values.

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td>ACMDRIVERDETAILS_SUPPORTF_ASYNC</td>
<td>Driver supports asynchronous conversions.</td>
</tr>
<tr>
<td>ACMDRIVERDETAILS_SUPPORTF_CODEC</td>
<td>Driver supports conversion between two different format tags. For example, if a driver supports compression from WAVE_FORMAT_PCM to WAVE_FORMAT_ADPCM, this flag is set.</td>
</tr>
<tr>
<td>ACMDRIVERDETAILS_SUPPORTF_CONVERTER</td>
<td>Driver supports conversion between two different formats of the same format tag. For example, if a driver supports resampling of WAVE_FORMAT_PCM, this flag is set.</td>
</tr>
<tr>
<td>ACMDRIVERDETAILS_SUPPORTF_DISABLED</td>
<td>Driver has been disabled. An application must specify the ACM_DRIVERENUMF_DISABLED flag with <a href="/windows/desktop/api/msacm/nf-msacm-acmdriverenum">acmDriverEnum</a> to include disabled drivers in the enumeration.</td>
</tr>
<tr>
<td>ACMDRIVERDETAILS_SUPPORTF_FILTER</td>
<td>Driver supports a filter (modification of the data without changing any of the format attributes). For example, if a driver supports volume or echo operations on WAVE_FORMAT_PCM, this flag is set.</td>
</tr>
</table>

## -returns

The callback function must return <b>TRUE</b> to continue enumeration or <b>FALSE</b> to stop enumeration.

## -remarks

The <a href="/windows/desktop/api/msacm/nf-msacm-acmdriverenum">acmDriverEnum</a> function will return MMSYSERR_NOERROR (zero) if no ACM drivers are installed. Moreover, the callback function will not be called.

The following functions should not be called from within the callback function: <a href="/windows/desktop/api/msacm/nf-msacm-acmdriveradd">acmDriverAdd</a>, <a href="/windows/desktop/api/msacm/nf-msacm-acmdriverremove">acmDriverRemove</a>, and <a href="/windows/desktop/api/msacm/nf-msacm-acmdriverpriority">acmDriverPriority</a>.

## -see-also

<a href="/windows/desktop/Multimedia/audio-compression-functions">Audio Compression Functions</a>



<a href="/windows/desktop/Multimedia/audio-compression-manager">Audio Compression Manager</a>