---
UID: NF:msacm.acmFilterTagEnumW
title: acmFilterTagEnumW function (msacm.h)
description: The acmFilterTagEnum (Unicode) function enumerates waveform-audio filter tags available from an ACM driver. This function continues enumerating until there are no more suitable filter tags or the callback function returns FALSE. (acmFilterTagEnumW)
helpviewer_keywords: ["_win32_acmFilterTagEnum", "acmFilterTagEnum", "acmFilterTagEnum function [Windows Multimedia]", "acmFilterTagEnumW", "msacm/acmFilterTagEnum", "msacm/acmFilterTagEnumW", "multimedia.acmfiltertagenum"]
old-location: multimedia\acmfiltertagenum.htm
tech.root: Multimedia
ms.assetid: eaec57c2-51b8-4842-ba78-f5726c2dc31d
ms.date: 08/02/2022
ms.keywords: _win32_acmFilterTagEnum, acmFilterTagEnum, acmFilterTagEnum function [Windows Multimedia], acmFilterTagEnumA, acmFilterTagEnumW, msacm/acmFilterTagEnum, msacm/acmFilterTagEnumA, msacm/acmFilterTagEnumW, multimedia.acmfiltertagenum
req.header: msacm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: acmFilterTagEnumW (Unicode) and acmFilterTagEnumA (ANSI)
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
 - acmFilterTagEnumW
 - msacm/acmFilterTagEnumW
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
 - acmFilterTagEnum
 - acmFilterTagEnumA
 - acmFilterTagEnumW
---

# acmFilterTagEnumW function


## -description

The <b>acmFilterTagEnum</b> function enumerates waveform-audio filter tags available from an ACM driver. This function continues enumerating until there are no more suitable filter tags or the callback function returns <b>FALSE</b>.

## -parameters

### -param had

Handle to the ACM driver to query for waveform-audio filter tag details. If this parameter is <b>NULL</b>, the ACM uses the details from the first suitable ACM driver.

### -param paftd

Pointer to the [ACMFILTERTAGDETAILS](./nf-msacm-acmfiltertagdetails.md) structure that contains the filter tag details when it is passed to the <b>fnCallback</b> function. When your application calls <b>acmFilterTagEnum</b>, the <b>cbStruct</b> member of this structure must be initialized.

### -param fnCallback

Procedure instance address of the application-defined callback function.

### -param dwInstance

A 64-bit (DWORD_PTR) or 32-bit (DWORD) application-defined value that is passed to the callback function along with ACM filter tag details.

### -param fdwEnum

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

## -remarks

This function will return MMSYSERR_NOERROR (zero) if no suitable ACM drivers are installed. Moreover, the callback function will not be called.





> [!NOTE]
> The msacm.h header defines acmFilterTagEnum as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Multimedia/audio-compression-functions">Audio Compression Functions</a>



<a href="/windows/desktop/Multimedia/audio-compression-manager">Audio Compression Manager</a>
