---
UID: NF:strmif.IDvdInfo2.GetDVDTextStringAsNative
title: IDvdInfo2::GetDVDTextStringAsNative (strmif.h)
description: The GetDVDTextStringAsNative method retrieves a DVD text string for a specified language, and returns the text string as an array of bytes.
helpviewer_keywords: ["GetDVDTextStringAsNative","GetDVDTextStringAsNative method [DirectShow]","GetDVDTextStringAsNative method [DirectShow]","IDvdInfo2 interface","IDvdInfo2 interface [DirectShow]","GetDVDTextStringAsNative method","IDvdInfo2.GetDVDTextStringAsNative","IDvdInfo2::GetDVDTextStringAsNative","IDvdInfo2GetDVDTextStringAsNative","dshow.idvdinfo2_getdvdtextstringasnative","strmif/IDvdInfo2::GetDVDTextStringAsNative"]
old-location: dshow\idvdinfo2_getdvdtextstringasnative.htm
tech.root: dshow
ms.assetid: a162b4ad-28f2-49fc-9b32-72538be9ddd5
ms.date: 4/26/2023
ms.keywords: GetDVDTextStringAsNative, GetDVDTextStringAsNative method [DirectShow], GetDVDTextStringAsNative method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetDVDTextStringAsNative method, IDvdInfo2.GetDVDTextStringAsNative, IDvdInfo2::GetDVDTextStringAsNative, IDvdInfo2GetDVDTextStringAsNative, dshow.idvdinfo2_getdvdtextstringasnative, strmif/IDvdInfo2::GetDVDTextStringAsNative
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
 - IDvdInfo2::GetDVDTextStringAsNative
 - strmif/IDvdInfo2::GetDVDTextStringAsNative
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
 - IDvdInfo2.GetDVDTextStringAsNative
---

# IDvdInfo2::GetDVDTextStringAsNative


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetDVDTextStringAsNative</code> method retrieves a DVD text string for a specified language, and returns the text string as an array of bytes.

## -parameters

### -param ulLangIndex [in]

Zero-based index of the language. To find the number of text-string languages on the DVD, call <a href="/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getdvdtextnumberoflanguages">IDvdInfo2::GetDVDTextNumberOfLanguages</a>.

### -param ulStringIndex [in]

Zero-based index of the string to retrieve. To find the number of strings for a given language, call <a href="/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo">IDvdInfo2::GetDVDTextLanguageInfo</a>.

### -param pbBuffer [out]

Pointer to a buffer that receives the text string. If <i>pchBuffer</i> is <b>NULL</b>, this method returns the size of the string in <i>pulActualSize</i>.

### -param ulMaxBufferSize [in]

Size of the <i>pchBuffer</i> in bytes

### -param pulActualSize [out]

Receives the actual length of the string in bytes, including the terminating <b>NULL</b>.

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

This method returns a DVD text string as a raw byte array, with no conversions. You can use this method to get text strings that are encoded using character sets other than Unicode or 7-bit ASCII (ISO/IEC 646), such as JIS Roman Kanji. To find the character set, call <a href="/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo">IDvdInfo2::GetDVDTextLanguageInfo</a>.

For Unicode and ASCII text strings, you can use the <a href="/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode">IDvdInfo2::GetDVDTextStringAsUnicode</a> method, which returns a wide-character string.

The returned string always includes a single terminating <b>NULL</b> byte. If the buffer is smaller than the length of the DVD text string, the string is truncated. To find the required size of the buffer, call the method once with <i>pchBuffer</i> equal to <b>NULL</b> and <i>ulMaxBufferSize</i> equal to zero. The size is returned in <i>pulActualSize</i>. Then allocate a buffer and call the method again.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2 Interface</a>



<a href="/windows/desktop/DirectShow/working-with-dvd-text-strings">Working with DVD Text Strings</a>