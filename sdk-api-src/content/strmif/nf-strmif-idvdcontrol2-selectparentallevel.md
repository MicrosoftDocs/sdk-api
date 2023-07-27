---
UID: NF:strmif.IDvdControl2.SelectParentalLevel
title: IDvdControl2::SelectParentalLevel (strmif.h)
description: The SelectParentalLevel method sets the parental access level for the logged-on user.
helpviewer_keywords: ["IDvdControl2 interface [DirectShow]","SelectParentalLevel method","IDvdControl2.SelectParentalLevel","IDvdControl2::SelectParentalLevel","IDvdControl2SelectParentalLevel","SelectParentalLevel","SelectParentalLevel method [DirectShow]","SelectParentalLevel method [DirectShow]","IDvdControl2 interface","dshow.idvdcontrol2_selectparentallevel","strmif/IDvdControl2::SelectParentalLevel"]
old-location: dshow\idvdcontrol2_selectparentallevel.htm
tech.root: dshow
ms.assetid: c87f8b12-0c14-4d3a-ac79-98577607d053
ms.date: 4/26/2023
ms.keywords: IDvdControl2 interface [DirectShow],SelectParentalLevel method, IDvdControl2.SelectParentalLevel, IDvdControl2::SelectParentalLevel, IDvdControl2SelectParentalLevel, SelectParentalLevel, SelectParentalLevel method [DirectShow], SelectParentalLevel method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_selectparentallevel, strmif/IDvdControl2::SelectParentalLevel
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
 - IDvdControl2::SelectParentalLevel
 - strmif/IDvdControl2::SelectParentalLevel
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
 - IDvdControl2.SelectParentalLevel
---

# IDvdControl2::SelectParentalLevel


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SelectParentalLevel</code> method sets the parental access level for the logged-on user.

## -parameters

### -param ulParentalLevel

Value that specifies the parental access level for the current user. For details, see Remarks.

## -returns

Returns one of the following values.

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
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
Invalid domain.

</td>
</tr>
</table>

## -remarks

There are eight generic parental levels defined in the DVD specification, numbered from 1 (most restrictive) through 8 (least restrictive). The meaning of these levels varies from region to region and depends on the current country/region (see <a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-selectparentalcountry">IDvdControl2::SelectParentalCountry</a>). For the United States and Canada (DVD Region 1), the suggested values are as follows:

<table>
<tr>
<td>Parental level
            </td>
<td>Meaning
            </td>
</tr>
<tr>
<td>1</td>
<td>The rating is G, general.</td>
</tr>
<tr>
<td>3</td>
<td>The rating is PG, parental guidance suggested.</td>
</tr>
<tr>
<td>4</td>
<td>The rating is PG-13, parental guidance suggested, not recommended for those under 13.</td>
</tr>
<tr>
<td>6</td>
<td>The rating is R, restricted.</td>
</tr>
<tr>
<td>7</td>
<td>The rating is NC-17, not appropriate for those under 17.</td>
</tr>
</table>
 

This method sets the current user's access level; this access level determines what content the user can play. Higher levels can play lower-level content; lower levels can't play higher-level content. In other words, adults can watch child-safe content, but children can't watch adult content.

DVD player applications can enforce restrictions on the parental level setting, such as providing password protection for raising the current parental level. The application's user interface should have a way to set the level and to disable checking completely. Some discs might be authored to disallow even level 8, meaning that no level is valid and no one could watch the disc if parental management is enabled. On such discs, parental management must be disabled for the discs to be viewed. Parental management in the <a href="/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> filter is disabled by default.

To disable parental management after it has been enabled, pass 0xffffffff for <i>ulParentalLevel</i>.

This method is demonstrated in the DVDSample application in <b>CDvdCore::SetParentalLevel</b>.

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

<table>
<tr>
<td>Annex J Command Name
            </td>
<td>Valid Domains
            </td>
</tr>
<tr>
<td>Parental_Level_Select</td>
<td>DVD_DOMAIN_Stop</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2 Interface</a>