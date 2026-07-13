---
UID: NF:strmif.IDvdInfo2.GetDVDTextStringAsUnicode
title: IDvdInfo2::GetDVDTextStringAsUnicode (strmif.h)
description: The GetDVDTextStringAsUnicode method retrieves a DVD text string for a specified language, and returns the text string as a Unicode string.
helpviewer_keywords: ["GetDVDTextStringAsUnicode","GetDVDTextStringAsUnicode method [DirectShow]","GetDVDTextStringAsUnicode method [DirectShow]","IDvdInfo2 interface","IDvdInfo2 interface [DirectShow]","GetDVDTextStringAsUnicode method","IDvdInfo2.GetDVDTextStringAsUnicode","IDvdInfo2::GetDVDTextStringAsUnicode","IDvdInfo2GetDVDTextStringAsUnicode","dshow.idvdinfo2_getdvdtextstringasunicode","strmif/IDvdInfo2::GetDVDTextStringAsUnicode"]
old-location: dshow\idvdinfo2_getdvdtextstringasunicode.htm
tech.root: dshow
ms.assetid: e13d4212-0e4a-40cf-89c7-f0c22f5a5cb9
ms.date: 4/26/2023
ms.keywords: GetDVDTextStringAsUnicode, GetDVDTextStringAsUnicode method [DirectShow], GetDVDTextStringAsUnicode method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetDVDTextStringAsUnicode method, IDvdInfo2.GetDVDTextStringAsUnicode, IDvdInfo2::GetDVDTextStringAsUnicode, IDvdInfo2GetDVDTextStringAsUnicode, dshow.idvdinfo2_getdvdtextstringasunicode, strmif/IDvdInfo2::GetDVDTextStringAsUnicode
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
 - IDvdInfo2::GetDVDTextStringAsUnicode
 - strmif/IDvdInfo2::GetDVDTextStringAsUnicode
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
 - IDvdInfo2.GetDVDTextStringAsUnicode
---

# IDvdInfo2::GetDVDTextStringAsUnicode


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetDVDTextStringAsUnicode</code> method retrieves a DVD text string for a specified language, and returns the text string as a Unicode string.

## -parameters

### -param ulLangIndex [in]

Zero-based index of the language. To find the number of text-string languages on the DVD, call <a href="/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getdvdtextnumberoflanguages">IDvdInfo2::GetDVDTextNumberOfLanguages</a>.

### -param ulStringIndex [in]

Zero-based index of the string to retrieve. To find the number of strings for a given language, call <a href="/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo">IDvdInfo2::GetDVDTextLanguageInfo</a>.

### -param pchwBuffer [out]

Pointer to a buffer that receives the text string. If <i>pchBuffer</i> is <b>NULL</b>, this method returns the size of the string in <i>pulActualSize</i>.

### -param ulMaxBufferSize [in]

Size of the <i>pchBuffer</i> buffer, in <b>WCHARs</b>.

### -param pulActualSize [out]

Receives the actual length of the string in characters, including the terminating <b>NULL</b>.

### -param pType [out]

Receives a member of the <a href="/windows/desktop/api/strmif/ne-strmif-dvd_textstringtype">DVD_TextStringType</a> enumeration. The value indicates the type of text string, such as movie title or song name. This parameter can also receive values that are not defined in the <b>DVD_TextStringType</b> enumeration.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Unsupported te

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
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
An unexpected internal error occurred.

</td>
</tr>
</table>

## -remarks

This method supports text strings that are encoded as Unicode or 7-bit ASCII (ISO/IEC 646). If the text string uses ASCII encoding, the method converts the string to a wide-character string. If the text string uses any other character set, the method returns E_FAIL. In that case, you can call <a href="/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative">IDvdInfo2::GetDVDTextStringAsNative</a> to retrieve the string as a raw byte array. To find the character set, call <a href="/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo">IDvdInfo2::GetDVDTextLanguageInfo</a>.

The returned string always includes a terminating <b>NULL</b>. If the buffer is smaller than the length of the DVD text string, the string is truncated. To find the required size of the buffer, call the method once with <i>pchBuffer</i> equal to <b>NULL</b> and <i>ulMaxBufferSize</i> equal to zero. The size is returned in <i>pulActualSize</i>. Then allocate a buffer and call the method again.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2 Interface</a>



<a href="/windows/desktop/DirectShow/working-with-dvd-text-strings">Working with DVD Text Strings</a>