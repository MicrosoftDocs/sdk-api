---
UID: NF:strmif.IDvdControl2.SelectDefaultSubpictureLanguage
title: IDvdControl2::SelectDefaultSubpictureLanguage (strmif.h)
description: The SelectDefaultSubpictureLanguage method sets the default language for subpicture text.
helpviewer_keywords: ["IDvdControl2 interface [DirectShow]","SelectDefaultSubpictureLanguage method","IDvdControl2.SelectDefaultSubpictureLanguage","IDvdControl2::SelectDefaultSubpictureLanguage","IDvdControl2SelectDefaultSubpictureLanguage","SelectDefaultSubpictureLanguage","SelectDefaultSubpictureLanguage method [DirectShow]","SelectDefaultSubpictureLanguage method [DirectShow]","IDvdControl2 interface","dshow.idvdcontrol2_selectdefaultsubpicturelanguage","strmif/IDvdControl2::SelectDefaultSubpictureLanguage"]
old-location: dshow\idvdcontrol2_selectdefaultsubpicturelanguage.htm
tech.root: dshow
ms.assetid: f49698cd-cc83-4f05-991d-2b3bba77c33a
ms.date: 4/26/2023
ms.keywords: IDvdControl2 interface [DirectShow],SelectDefaultSubpictureLanguage method, IDvdControl2.SelectDefaultSubpictureLanguage, IDvdControl2::SelectDefaultSubpictureLanguage, IDvdControl2SelectDefaultSubpictureLanguage, SelectDefaultSubpictureLanguage, SelectDefaultSubpictureLanguage method [DirectShow], SelectDefaultSubpictureLanguage method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_selectdefaultsubpicturelanguage, strmif/IDvdControl2::SelectDefaultSubpictureLanguage
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
 - IDvdControl2::SelectDefaultSubpictureLanguage
 - strmif/IDvdControl2::SelectDefaultSubpictureLanguage
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
 - IDvdControl2.SelectDefaultSubpictureLanguage
---

# IDvdControl2::SelectDefaultSubpictureLanguage


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SelectDefaultSubpictureLanguage</code> method sets the default language for subpicture text.

## -parameters

### -param Language [in]

Locale identifier that specifies the default language.

### -param subpictureExtension [in]

[DVD_SUBPICTURE_LANG_EXT](/windows/desktop/api/strmif/ne-strmif-dvd_subpicture_lang_ext) enumeration that specifies the default subpicture extension.

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
<i>Language</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> filter is not in a valid domain.

</td>
</tr>
</table>

## -remarks

This method selects the default language and format to use for subpictures and menus when the disc is played. For example, if <i>Language</i> is specified as 0x409 for U.S. English and <i>subpictureExtension</i> is specified as DVD_SP_EXT_Caption_Big, the DVD Navigator tries to show U.S. English text in the "big caption" format in subpictures. If the default language or language extension is not found on a disc, the DVD Navigator selects the closest match.

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

<table>
<tr>
<td>Annex J Command Name
            </td>
<td>Valid Domains
            </td>
</tr>
<tr>
<td>None</td>
<td>DVD_DOMAIN_Stop</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2 Interface</a>