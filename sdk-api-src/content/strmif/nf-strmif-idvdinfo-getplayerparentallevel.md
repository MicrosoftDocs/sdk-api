---
UID: NF:strmif.IDvdInfo.GetPlayerParentalLevel
title: IDvdInfo::GetPlayerParentalLevel (strmif.h)
description: Note  The IDvdInfo interface is deprecated. Use IDvdInfo2 instead. Retrieves the current parental level and country/region code settings for the DVD player.
helpviewer_keywords: ["GetPlayerParentalLevel","GetPlayerParentalLevel method [DirectShow]","GetPlayerParentalLevel method [DirectShow]","IDvdInfo interface","IDvdInfo interface [DirectShow]","GetPlayerParentalLevel method","IDvdInfo.GetPlayerParentalLevel","IDvdInfo::GetPlayerParentalLevel","IDvdInfoGetPlayerParentalLevel","dshow.idvdinfo_getplayerparentallevel","strmif/IDvdInfo::GetPlayerParentalLevel"]
old-location: dshow\idvdinfo_getplayerparentallevel.htm
tech.root: dshow
ms.assetid: 2b4111db-fbb1-4da7-85e1-ddd3f5718225
ms.date: 4/26/2023
ms.keywords: GetPlayerParentalLevel, GetPlayerParentalLevel method [DirectShow], GetPlayerParentalLevel method [DirectShow],IDvdInfo interface, IDvdInfo interface [DirectShow],GetPlayerParentalLevel method, IDvdInfo.GetPlayerParentalLevel, IDvdInfo::GetPlayerParentalLevel, IDvdInfoGetPlayerParentalLevel, dshow.idvdinfo_getplayerparentallevel, strmif/IDvdInfo::GetPlayerParentalLevel
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
 - IDvdInfo::GetPlayerParentalLevel
 - strmif/IDvdInfo::GetPlayerParentalLevel
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
 - IDvdInfo.GetPlayerParentalLevel
---

# IDvdInfo::GetPlayerParentalLevel


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <b>IDvdInfo</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2</a> instead.</div>
<div> </div>
Retrieves the current parental level and country/region code settings for the DVD player.

## -parameters

### -param pulParentalLevel [out]

Pointer to a value indicating the current parental level.

### -param pulCountryCode [out]

Pointer to a value indicating the current country/region code.

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

For the defined parental levels, see Table 3.3.4-1 of the DVD-Video specification.

Valid parental levels are 1 through 8 if parental management is enabled, 0xffffffff if parental management is disabled.

For the country/region codes, see ISO3166 : Alpha-2 Code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo">IDvdInfo Interface</a>