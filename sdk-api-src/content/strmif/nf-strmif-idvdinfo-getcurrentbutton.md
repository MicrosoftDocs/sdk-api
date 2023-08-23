---
UID: NF:strmif.IDvdInfo.GetCurrentButton
title: IDvdInfo::GetCurrentButton (strmif.h)
description: Note  The IDvdInfo interface is deprecated. Use IDvdInfo2 instead. Retrieves the number of available buttons and the currently selected button number.
helpviewer_keywords: ["GetCurrentButton","GetCurrentButton method [DirectShow]","GetCurrentButton method [DirectShow]","IDvdInfo interface","IDvdInfo interface [DirectShow]","GetCurrentButton method","IDvdInfo.GetCurrentButton","IDvdInfo::GetCurrentButton","IDvdInfoGetCurrentButton","dshow.idvdinfo_getcurrentbutton","strmif/IDvdInfo::GetCurrentButton"]
old-location: dshow\idvdinfo_getcurrentbutton.htm
tech.root: dshow
ms.assetid: 13df79ea-81c9-4060-8e11-ad7a24a7b5fa
ms.date: 4/26/2023
ms.keywords: GetCurrentButton, GetCurrentButton method [DirectShow], GetCurrentButton method [DirectShow],IDvdInfo interface, IDvdInfo interface [DirectShow],GetCurrentButton method, IDvdInfo.GetCurrentButton, IDvdInfo::GetCurrentButton, IDvdInfoGetCurrentButton, dshow.idvdinfo_getcurrentbutton, strmif/IDvdInfo::GetCurrentButton
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
 - IDvdInfo::GetCurrentButton
 - strmif/IDvdInfo::GetCurrentButton
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
 - IDvdInfo.GetCurrentButton
---

# IDvdInfo::GetCurrentButton


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <b>IDvdInfo</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2</a> instead.</div>
<div> </div>
Retrieves the number of available buttons and the currently selected button number.

## -parameters

### -param pulButtonsAvailable [out]

Pointer to the number of buttons available.

### -param pulCurrentButton [out]

Pointer to the number of the current button.

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
<dt><b>VFW_E_DVD_OPERATION_INHIBITED</b></dt>
</dl>
</td>
<td width="60%">
Requested action cannot occur at this point in the movie due to the authoring of the current DVD-Video disc.

</td>
</tr>
</table>

## -remarks

If buttons are not present this method returns zero for both <i>pnButtonsAvailable</i> and <i>pnCurrentButton</i>.

This method is valid in any domain. For more information, see <a href="/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo">IDvdInfo Interface</a>