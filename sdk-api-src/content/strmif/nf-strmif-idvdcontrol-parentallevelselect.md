---
UID: NF:strmif.IDvdControl.ParentalLevelSelect
title: IDvdControl::ParentalLevelSelect (strmif.h)
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Sets the parental access level for the current media file.
helpviewer_keywords: ["IDvdControl interface [DirectShow]","ParentalLevelSelect method","IDvdControl.ParentalLevelSelect","IDvdControl::ParentalLevelSelect","IDvdControlParentalLevelSelect","ParentalLevelSelect","ParentalLevelSelect method [DirectShow]","ParentalLevelSelect method [DirectShow]","IDvdControl interface","dshow.idvdcontrol_parentallevelselect","strmif/IDvdControl::ParentalLevelSelect"]
old-location: dshow\idvdcontrol_parentallevelselect.htm
tech.root: dshow
ms.assetid: ca572d89-b188-442d-884f-0cffa71c2892
ms.date: 4/26/2023
ms.keywords: IDvdControl interface [DirectShow],ParentalLevelSelect method, IDvdControl.ParentalLevelSelect, IDvdControl::ParentalLevelSelect, IDvdControlParentalLevelSelect, ParentalLevelSelect, ParentalLevelSelect method [DirectShow], ParentalLevelSelect method [DirectShow],IDvdControl interface, dshow.idvdcontrol_parentallevelselect, strmif/IDvdControl::ParentalLevelSelect
req.header: strmif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Reference:\_Dshowh
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
req.dll: Quartz.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDvdControl::ParentalLevelSelect
 - strmif/IDvdControl::ParentalLevelSelect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Quartz.dll
api_name:
 - IDvdControl.ParentalLevelSelect
---

# IDvdControl::ParentalLevelSelect


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a> instread.</div>
<div> </div>
Sets the parental access level for the current media file.

## -parameters

### -param ulParentalLevel

Value that specifies the current media file parental access level. Should be a value from 1 to 8, inclusive. Predefined parental levels are as follows:

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>1</td>
<td>The rating is G, General.</td>
</tr>
<tr>
<td>3</td>
<td>The rating is PG, Parental Guidance Suggested.</td>
</tr>
<tr>
<td>4</td>
<td>The rating is PG-13, Parental Guidance Suggested, not recommended for those under 13.</td>
</tr>
<tr>
<td>6</td>
<td>The rating is R, Restricted.</td>
</tr>
<tr>
<td>7</td>
<td>The rating is NC-17.</td>
</tr>
</table>

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

This method returns an error unless the domain is DVD_DOMAIN_Stop. For more information, see <a href="/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.

This method sets the current user's access level; this access level determines what media files the user can play back. Higher levels can play lower-level content; lower levels can't play higher-level content. For example, adults can watch child-safe content, but children can't watch adult content.

The <a href="/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> filter provides no restriction on setting the parental level. DVD player applications can enforce restrictions on the parental level setting, such as providing password protection for raising the current parental level. Parental management in the DVD Navigator is disabled by default.

To disable parental management, pass 0xffffffff for <i>ulParentalLevel</i>. If parental management is disabled, then the player will play the first program chain (PGC) in a parental block regardless of parental IDs.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol">IDvdControl Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-parentalcountryselect">IDvdControl::ParentalCountrySelect</a>