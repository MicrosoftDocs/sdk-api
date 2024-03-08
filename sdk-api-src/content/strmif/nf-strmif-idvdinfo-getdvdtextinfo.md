---
UID: NF:strmif.IDvdInfo.GetDVDTextInfo
title: IDvdInfo::GetDVDTextInfo (strmif.h)
description: Note  The IDvdInfo interface is deprecated. Use IDvdInfo2 instead. Retrieves the TXTDT_MG structure, which can contain text descriptions for title name, volume name, producer name, vocalist name, and so on, in various languages.
helpviewer_keywords: ["GetDVDTextInfo","GetDVDTextInfo method [DirectShow]","GetDVDTextInfo method [DirectShow]","IDvdInfo interface","IDvdInfo interface [DirectShow]","GetDVDTextInfo method","IDvdInfo.GetDVDTextInfo","IDvdInfo::GetDVDTextInfo","IDvdInfoGetDVDTextInfo","dshow.idvdinfo_getdvdtextinfo","strmif/IDvdInfo::GetDVDTextInfo"]
old-location: dshow\idvdinfo_getdvdtextinfo.htm
tech.root: dshow
ms.assetid: e58fcd07-682a-4c41-9501-d55ba092a150
ms.date: 4/26/2023
ms.keywords: GetDVDTextInfo, GetDVDTextInfo method [DirectShow], GetDVDTextInfo method [DirectShow],IDvdInfo interface, IDvdInfo interface [DirectShow],GetDVDTextInfo method, IDvdInfo.GetDVDTextInfo, IDvdInfo::GetDVDTextInfo, IDvdInfoGetDVDTextInfo, dshow.idvdinfo_getdvdtextinfo, strmif/IDvdInfo::GetDVDTextInfo
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
 - IDvdInfo::GetDVDTextInfo
 - strmif/IDvdInfo::GetDVDTextInfo
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
 - IDvdInfo.GetDVDTextInfo
---

# IDvdInfo::GetDVDTextInfo


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <b>IDvdInfo</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2</a> instead.</div>
<div> </div>
Retrieves the <b>TXTDT_MG</b> structure, which can contain text descriptions for title name, volume name, producer name, vocalist name, and so on, in various languages.

## -parameters

### -param pTextManager [out]

Pointer to the retrieved text manager.

### -param ulBufSize [in]

Size of the buffer for <i>pTextManager</i>, in bytes.

### -param pulActualSize [out]

Pointer to a value containing the number of bytes of data returned.

## -returns

Returns an <b>HRESULT</b> value .

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

If the supplied buffer size in <i>cbBufSize</i> is too small for the data, (for example if <i>cbBufSize</i> equals zero), then this method returns E_OUTOFMEMORY and sets the value pointed to by <i>pcbActualSize</i> to the required size.

For more information, refer to Section 4.1.6 and Annex A of the DVD-Video specification.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo">IDvdInfo Interface</a>