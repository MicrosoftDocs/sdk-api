---
UID: NF:qnetwork.IAMExtendedSeeking.get_ExSeekCapabilities
title: IAMExtendedSeeking::get_ExSeekCapabilities (qnetwork.h)
description: The get_ExSeekCapabilities method retrieves the extended seeking capabilities of the filter.
helpviewer_keywords: ["IAMExtendedSeeking interface [DirectShow]","get_ExSeekCapabilities method","IAMExtendedSeeking.get_ExSeekCapabilities","IAMExtendedSeeking::get_ExSeekCapabilities","IAMExtendedSeekingget_ExSeekCapabilities","dshow.iamextendedseeking_get_exseekcapabilities","get_ExSeekCapabilities","get_ExSeekCapabilities method [DirectShow]","get_ExSeekCapabilities method [DirectShow]","IAMExtendedSeeking interface","qnetwork/IAMExtendedSeeking::get_ExSeekCapabilities"]
old-location: dshow\iamextendedseeking_get_exseekcapabilities.htm
tech.root: dshow
ms.assetid: caae9e8c-6d42-4bbc-a66a-bdde1009469d
ms.date: 12/05/2018
ms.keywords: IAMExtendedSeeking interface [DirectShow],get_ExSeekCapabilities method, IAMExtendedSeeking.get_ExSeekCapabilities, IAMExtendedSeeking::get_ExSeekCapabilities, IAMExtendedSeekingget_ExSeekCapabilities, dshow.iamextendedseeking_get_exseekcapabilities, get_ExSeekCapabilities, get_ExSeekCapabilities method [DirectShow], get_ExSeekCapabilities method [DirectShow],IAMExtendedSeeking interface, qnetwork/IAMExtendedSeeking::get_ExSeekCapabilities
req.header: qnetwork.h
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
 - IAMExtendedSeeking::get_ExSeekCapabilities
 - qnetwork/IAMExtendedSeeking::get_ExSeekCapabilities
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Qnetwork.h
api_name:
 - IAMExtendedSeeking.get_ExSeekCapabilities
---

# IAMExtendedSeeking::get_ExSeekCapabilities


## -description

The <code>get_ExSeekCapabilities</code> method retrieves the extended seeking capabilities of the filter.

## -parameters

### -param pExCapabilities [out]

Pointer to a variable that receives a bitwise OR of <a href="/windows/desktop/api/qnetwork/ne-qnetwork-amextendedseekingcapabilities">AMExtendedSeekingCapabilities</a> flags.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

The Windows Media Source filter sets the extended seeking flags as follows.

<table>
<tr>
<td>Flag
            </td>
<td>Condition
            </td>
</tr>
<tr>
<td>AM_EXSEEK_BUFFERING</td>
<td>Always.</td>
</tr>
<tr>
<td>AM_EXSEEK_NOSTANDARDREPAINT</td>
<td>Always.</td>
</tr>
<tr>
<td>AM_EXSEEK_SENDS_VIDEOFRAMEREADY</td>
<td>If the video pin has been created.</td>
</tr>
<tr>
<td>AM_EXSEEK_CANSCAN, AM_EXSEEK_SCANWITHOUTCLOCK</td>
<td>If the stream supports rates other than 1.0.</td>
</tr>
<tr>
<td>AM_EXSEEK_CANSEEK</td>
<td>If the stream has been authored to be seekable.</td>
</tr>
<tr>
<td>AM_EXSEEK_MARKERSEEK</td>
<td>If the stream contains markers.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamextendedseeking">IAMExtendedSeeking Interface</a>