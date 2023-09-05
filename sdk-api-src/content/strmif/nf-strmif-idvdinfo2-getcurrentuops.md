---
UID: NF:strmif.IDvdInfo2.GetCurrentUOPS
title: IDvdInfo2::GetCurrentUOPS (strmif.h)
description: The GetCurrentUOPS method retrieves a set of flags indicating which navigation commands, if any, the content authors have explicitly disabled for the current disc location.
helpviewer_keywords: ["GetCurrentUOPS","GetCurrentUOPS method [DirectShow]","GetCurrentUOPS method [DirectShow]","IDvdInfo2 interface","IDvdInfo2 interface [DirectShow]","GetCurrentUOPS method","IDvdInfo2.GetCurrentUOPS","IDvdInfo2::GetCurrentUOPS","IDvdInfo2GetCurrentUOPS","dshow.idvdinfo2_getcurrentuops","strmif/IDvdInfo2::GetCurrentUOPS"]
old-location: dshow\idvdinfo2_getcurrentuops.htm
tech.root: dshow
ms.assetid: 71ae88f0-17ad-4530-b2e7-6a8155c14a97
ms.date: 4/26/2023
ms.keywords: GetCurrentUOPS, GetCurrentUOPS method [DirectShow], GetCurrentUOPS method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetCurrentUOPS method, IDvdInfo2.GetCurrentUOPS, IDvdInfo2::GetCurrentUOPS, IDvdInfo2GetCurrentUOPS, dshow.idvdinfo2_getcurrentuops, strmif/IDvdInfo2::GetCurrentUOPS
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDvdInfo2::GetCurrentUOPS
 - strmif/IDvdInfo2::GetCurrentUOPS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDvdInfo2.GetCurrentUOPS
---

# IDvdInfo2::GetCurrentUOPS


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetCurrentUOPS</code> method retrieves a set of flags indicating which navigation commands, if any, the content authors have explicitly disabled for the current disc location.

## -parameters

### -param pulUOPs [out]

Receives a bitwise [VALID_UOP_FLAG](/windows/desktop/api/strmif/ne-strmif-valid_uop_flag) values. Each bit represents the state (valid or not valid) of a user operation (UOP). If the bit is set, then that user operation is prohibited. See Remarks.

## -returns

Returns one of the following <b>HRESULT</b> values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pulUOPs</i> is not a valid pointer.

</td>
</tr>
</table>

## -remarks

DVD authors can insert UOP commands at almost any place on the disc to disallow a navigation command that would otherwise be permitted within the current DVD domain. In other words, UOP commands enable disc authors to override the usual navigation permissions.

A DVD player application should normally never have to use this method because the DVD Navigator automatically checks all UOP permissions before proceeding with any command, and will return VFW_E_DVD_OPERATION_INHIBITED from any method if the command is invalid under the current UOP. If your application needs to track the current UOP permissions itself, you can call <code>GetCurrentUOPS</code> whenever the current UOP permissions are required, or you can handle the <a href="/windows/desktop/DirectShow/ec-dvd-valid-uops-change">EC_DVD_VALID_UOPS_CHANGE</a> event notification in your message loop and retrieve the UOP information from the <i>lParam1</i> parameter. The latter approach is generally more efficient.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2 Interface</a>