---
UID: NF:strmif.IDvdInfo.GetAllGPRMs
title: IDvdInfo::GetAllGPRMs (strmif.h)
description: Note  The IDvdInfo interface is deprecated. Use IDvdInfo2 instead. Retrieves the current contents of all general parameter registers (GPRMs).
helpviewer_keywords: ["GetAllGPRMs","GetAllGPRMs method [DirectShow]","GetAllGPRMs method [DirectShow]","IDvdInfo interface","IDvdInfo interface [DirectShow]","GetAllGPRMs method","IDvdInfo.GetAllGPRMs","IDvdInfo::GetAllGPRMs","IDvdInfoGetAllGPRMs","dshow.idvdinfo_getallgprms","strmif/IDvdInfo::GetAllGPRMs"]
old-location: dshow\idvdinfo_getallgprms.htm
tech.root: dshow
ms.assetid: 87d82404-cd43-4499-abc2-6c043c43bf4e
ms.date: 4/26/2023
ms.keywords: GetAllGPRMs, GetAllGPRMs method [DirectShow], GetAllGPRMs method [DirectShow],IDvdInfo interface, IDvdInfo interface [DirectShow],GetAllGPRMs method, IDvdInfo.GetAllGPRMs, IDvdInfo::GetAllGPRMs, IDvdInfoGetAllGPRMs, dshow.idvdinfo_getallgprms, strmif/IDvdInfo::GetAllGPRMs
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IDvdInfo::GetAllGPRMs
 - strmif/IDvdInfo::GetAllGPRMs
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IDvdInfo.GetAllGPRMs
---

# IDvdInfo::GetAllGPRMs


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <b>IDvdInfo</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2</a> instead.</div>
<div> </div>
Retrieves the current contents of all general parameter registers (GPRMs).

## -parameters

### -param pRegisterArray [out]

Pointer to the retrieved array of general parameter registers.

## -returns

Returns an <b>HRESULT</b> value.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
DVD is not initialized or domain is not DVD_DOMAIN_Title.

</td>
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
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
Requested action is not supported on this domain (<a href="/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_OPERATION_INHIBITED</b></dt>
</dl>
</td>
<td width="60%">
Requested action cannot occur at this point in the movie due to the authoring of the current DVD-Video disc.

</td>
</tr>
</table>

## -remarks

This method is valid in any domain. For more information, see <a href="/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.

Use of GPRMs is title specific. GPRMs are general parameter registers. For an explanation of GPRMs, see the DVD specifications.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo">IDvdInfo Interface</a>