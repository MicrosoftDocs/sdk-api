---
UID: NF:strmif.IDvdInfo2.GetState
title: IDvdInfo2::GetState (strmif.h)
description: The GetState method retrieves a bookmark containing the disc location and DVD Navigator state information.
helpviewer_keywords: ["GetState","GetState method [DirectShow]","GetState method [DirectShow]","IDvdInfo2 interface","IDvdInfo2 interface [DirectShow]","GetState method","IDvdInfo2.GetState","IDvdInfo2::GetState","IDvdInfo2GetState","dshow.idvdinfo2_getstate","strmif/IDvdInfo2::GetState"]
old-location: dshow\idvdinfo2_getstate.htm
tech.root: dshow
ms.assetid: 403add2b-3dfd-436d-8184-7a14f30f6ea3
ms.date: 4/26/2023
ms.keywords: GetState, GetState method [DirectShow], GetState method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetState method, IDvdInfo2.GetState, IDvdInfo2::GetState, IDvdInfo2GetState, dshow.idvdinfo2_getstate, strmif/IDvdInfo2::GetState
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
 - IDvdInfo2::GetState
 - strmif/IDvdInfo2::GetState
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
 - IDvdInfo2.GetState
---

# IDvdInfo2::GetState


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetState</code> method retrieves a bookmark containing the disc location and DVD Navigator state information.

## -parameters

### -param pStateData [out]

Receives a pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-idvdstate">IDvdState</a> interface of a <b>DvdState</b> object allocated by the DVD Navigator.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
DVD Navigator is not initialized.

</td>
</tr>
</table>

## -remarks

When this method is called, the DVD Navigator creates a new state object and saves the current location into it, as well as the current parental level and other state information. The <b>DVDState</b> object can be used to restore the DVD Navigator to the saved location at a later time through a call to <a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-setstate">IDvdControl2::SetState</a>. This enables viewers to stop viewing in the middle of a disc, save the location, and come back at some later time to begin viewing where they left off, with all the internal settings restored as they were before.

The DVD Navigator calls <b>AddRef</b> on the <b>DvdState</b> object before returning it to the application. The application must call <b>Release</b> on the object when it is finished with it.

This method is demonstrated in the DVDSample application in <b>CDvdCore::RestoreBookmark</b>.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2 Interface</a>