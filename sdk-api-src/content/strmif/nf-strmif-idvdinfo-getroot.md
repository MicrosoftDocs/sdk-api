---
UID: NF:strmif.IDvdInfo.GetRoot
title: IDvdInfo::GetRoot (strmif.h)
description: Note  The IDvdInfo interface is deprecated. Use IDvdInfo2 instead. Retrieves the root directory that is set in the player.
helpviewer_keywords: ["GetRoot","GetRoot method [DirectShow]","GetRoot method [DirectShow]","IDvdInfo interface","IDvdInfo interface [DirectShow]","GetRoot method","IDvdInfo.GetRoot","IDvdInfo::GetRoot","IDvdInfoGetRoot","dshow.idvdinfo_getroot","strmif/IDvdInfo::GetRoot"]
old-location: dshow\idvdinfo_getroot.htm
tech.root: dshow
ms.assetid: e3869da3-15c9-449e-bb0e-29dd4625a857
ms.date: 4/26/2023
ms.keywords: GetRoot, GetRoot method [DirectShow], GetRoot method [DirectShow],IDvdInfo interface, IDvdInfo interface [DirectShow],GetRoot method, IDvdInfo.GetRoot, IDvdInfo::GetRoot, IDvdInfoGetRoot, dshow.idvdinfo_getroot, strmif/IDvdInfo::GetRoot
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
 - IDvdInfo::GetRoot
 - strmif/IDvdInfo::GetRoot
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
 - IDvdInfo.GetRoot
---

# IDvdInfo::GetRoot


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <b>IDvdInfo</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2</a> instead.</div>
<div> </div>
Retrieves the root directory that is set in the player.

## -parameters

### -param pRoot [out]

Pointer to the buffer to receive the root string. Note that the root string uses ANSI characters.

### -param ulBufSize [in]

Size of buffer passed in, in bytes.

### -param pulActualSize [out]

Pointer to a value containing the size of the actual data returned.

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

If a valid root was found, this method returns the root string. Otherwise, it returns zero for <i>pcbActualSize</i>, indicating that a valid root directory has not been found or initialized.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo">IDvdInfo Interface</a>