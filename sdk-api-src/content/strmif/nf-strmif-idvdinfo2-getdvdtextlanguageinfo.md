---
UID: NF:strmif.IDvdInfo2.GetDVDTextLanguageInfo
title: IDvdInfo2::GetDVDTextLanguageInfo (strmif.h)
description: The GetDVDTextLanguageInfo method retrieves information about the text strings for a specified language. The method retrieves the number of strings for that language, the locale identifier, and the character set.
helpviewer_keywords: ["GetDVDTextLanguageInfo","GetDVDTextLanguageInfo method [DirectShow]","GetDVDTextLanguageInfo method [DirectShow]","IDvdInfo2 interface","IDvdInfo2 interface [DirectShow]","GetDVDTextLanguageInfo method","IDvdInfo2.GetDVDTextLanguageInfo","IDvdInfo2::GetDVDTextLanguageInfo","IDvdInfo2GetDVDTextLanguageInfo","dshow.idvdinfo2_getdvdtextlanguageinfo","strmif/IDvdInfo2::GetDVDTextLanguageInfo"]
old-location: dshow\idvdinfo2_getdvdtextlanguageinfo.htm
tech.root: dshow
ms.assetid: af8662af-f306-4142-b563-3b40a98b7fbe
ms.date: 4/26/2023
ms.keywords: GetDVDTextLanguageInfo, GetDVDTextLanguageInfo method [DirectShow], GetDVDTextLanguageInfo method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetDVDTextLanguageInfo method, IDvdInfo2.GetDVDTextLanguageInfo, IDvdInfo2::GetDVDTextLanguageInfo, IDvdInfo2GetDVDTextLanguageInfo, dshow.idvdinfo2_getdvdtextlanguageinfo, strmif/IDvdInfo2::GetDVDTextLanguageInfo
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
 - IDvdInfo2::GetDVDTextLanguageInfo
 - strmif/IDvdInfo2::GetDVDTextLanguageInfo
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
 - IDvdInfo2.GetDVDTextLanguageInfo
---

# IDvdInfo2::GetDVDTextLanguageInfo


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetDVDTextLanguageInfo</code> method retrieves information about the text strings for a specified language. The method retrieves the number of strings for that language, the locale identifier, and the character set.

## -parameters

### -param ulLangIndex [in]

Zero-based index of the language to query. To find the number of text-string languages on the DVD, call <a href="/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getdvdtextnumberoflanguages">IDvdInfo2::GetDVDTextNumberOfLanguages</a>.

### -param pulNumOfStrings [out]

Receives the number of text strings for the specified language.

### -param pLangCode [out]

Receives a <i>locale identifier</i> (LCID) that specifies the language in which the text is written. For example, the LCID for "en-us" is 0x0409.

### -param pbCharacterSet [out]

Receives a member of the <a href="/windows/desktop/api/strmif/ne-strmif-dvd_textcharset">DVD_TextCharSet</a> enumeration. The value specifies the character set of the text string.

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
This DVD does not have any text strings, or the <i>ulLangIndex</i> parameter is out of bounds.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected internal error occurred.

</td>
</tr>
</table>

## -remarks

To get a particular text string, call <a href="/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode">IDvdInfo2::GetDVDTextStringAsUnicode</a> or <a href="/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative">IDvdInfo2::GetDVDTextStringAsNative</a>.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2 Interface</a>



<a href="/windows/desktop/DirectShow/working-with-dvd-text-strings">Working with DVD Text Strings</a>