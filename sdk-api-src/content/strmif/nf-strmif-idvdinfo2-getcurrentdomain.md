---
UID: NF:strmif.IDvdInfo2.GetCurrentDomain
title: IDvdInfo2::GetCurrentDomain (strmif.h)
description: The GetCurrentDomain method retrieves the domain in which the DVD Navigator is currently located.
helpviewer_keywords: ["GetCurrentDomain","GetCurrentDomain method [DirectShow]","GetCurrentDomain method [DirectShow]","IDvdInfo2 interface","IDvdInfo2 interface [DirectShow]","GetCurrentDomain method","IDvdInfo2.GetCurrentDomain","IDvdInfo2::GetCurrentDomain","IDvdInfo2GetCurrentDomain","dshow.idvdinfo2_getcurrentdomain","strmif/IDvdInfo2::GetCurrentDomain"]
old-location: dshow\idvdinfo2_getcurrentdomain.htm
tech.root: dshow
ms.assetid: ad850402-7b48-4517-a55f-42cfa75d3ee6
ms.date: 4/26/2023
ms.keywords: GetCurrentDomain, GetCurrentDomain method [DirectShow], GetCurrentDomain method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetCurrentDomain method, IDvdInfo2.GetCurrentDomain, IDvdInfo2::GetCurrentDomain, IDvdInfo2GetCurrentDomain, dshow.idvdinfo2_getcurrentdomain, strmif/IDvdInfo2::GetCurrentDomain
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
 - IDvdInfo2::GetCurrentDomain
 - strmif/IDvdInfo2::GetCurrentDomain
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
 - IDvdInfo2.GetCurrentDomain
---

# IDvdInfo2::GetCurrentDomain


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetCurrentDomain</code> method retrieves the domain in which the <a href="/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> is currently located.

## -parameters

### -param pDomain [out]

Pointer to a variable of type <a href="/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a> that receives the current domain.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
</table>

## -remarks

You can use this method to test whether the DVD Navigator is finished playing in a particular title domain. An application doesn't have to test for the current domain before calling an <a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a> method such as <a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-playtitle">PlayTitle</a>, <a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-playforwards">PlayForwards</a>, and so on. The DVD Navigator tests for the domain and simply does nothing, returning VFW_E_DVD_INVALIDDOMAIN, if the current command is invalid for the domain.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/ec-dvd-domain-change">EC_DVD_DOMAIN_CHANGE</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2 Interface</a>