---
UID: NF:msacm.acmFilterChooseA
title: acmFilterChooseA function (msacm.h)
description: The acmFilterChoose function creates an ACM-defined dialog box that enables the user to select a waveform-audio filter. (acmFilterChooseA)
helpviewer_keywords: ["acmFilterChooseA", "msacm/acmFilterChooseA"]
old-location: multimedia\acmfilterchoose.htm
tech.root: Multimedia
ms.assetid: 9d8f659f-46f7-4399-a538-24c887c0fbee
ms.date: 12/05/2018
ms.keywords: _win32_acmFilterChoose, acmFilterChoose, acmFilterChoose function [Windows Multimedia], acmFilterChooseA, acmFilterChooseW, msacm/acmFilterChoose, msacm/acmFilterChooseA, msacm/acmFilterChooseW, multimedia.acmfilterchoose
req.header: msacm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: acmFilterChooseW (Unicode) and acmFilterChooseA (ANSI)
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
 - acmFilterChooseA
 - msacm/acmFilterChooseA
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
 - acmFilterChoose
 - acmFilterChooseA
 - acmFilterChooseW
---

# acmFilterChooseA function


## -description

The <b>acmFilterChoose</b> function creates an ACM-defined dialog box that enables the user to select a waveform-audio filter.

## -parameters

### -param pafltrc

Pointer to an [ACMFILTERCHOOSE](./nf-msacm-acmfilterchoose.md) structure that contains information used to initialize the dialog box. When <b>acmFilterChoose</b> returns, this structure contains information about the user's filter selection.

The <b>pwfltr</b> member of this structure must contain a valid pointer to a memory location that will contain the returned filter header structure. The <b>cbwfltr</b> member must be filled in with the size, in bytes, of this memory buffer.

## -returns

Returns MMSYSERR_NOERROR if successful or an error otherwise. Possible error values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ACMERR_CANCELED</b></dt>
</dl>
</td>
<td width="60%">
The user chose the Cancel button or the Close command on the System menu to close the dialog box.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ACMERR_NOTPOSSIBLE</b></dt>
</dl>
</td>
<td width="60%">
The buffer identified by the [ACMFILTERCHOOSE](./nf-msacm-acmfilterchoose.md) structure is too small to contain the selected filter.

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
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_NODRIVER</b></dt>
</dl>
</td>
<td width="60%">
A suitable driver is not available to provide valid filter selections.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/Multimedia/audio-compression-functions">Audio Compression Functions</a>



<a href="/windows/desktop/Multimedia/audio-compression-manager">Audio Compression Manager</a>

## -remarks

> [!NOTE]
> The msacm.h header defines ACMFILTERCHOOSE as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
