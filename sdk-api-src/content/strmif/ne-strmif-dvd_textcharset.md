---
UID: NE:strmif.DVD_TextCharSet
title: DVD_TextCharSet (strmif.h)
description: Defines which character set a specified string is encoded with.
helpviewer_keywords: ["DVD_CharSet_ISO646","DVD_CharSet_ISO8859_1","DVD_CharSet_JIS_Roman_Kanji","DVD_CharSet_ShiftJIS_Kanji_Roman_Katakana","DVD_CharSet_Unicode","DVD_TextCharSet","DVD_TextCharSet","DVD_TextCharSet enumeration [DirectShow]","DVD_TextCharSetEnumeration","dshow.dvd_textcharset","strmif/DVD_CharSet_ISO646","strmif/DVD_CharSet_ISO8859_1","strmif/DVD_CharSet_JIS_Roman_Kanji","strmif/DVD_CharSet_ShiftJIS_Kanji_Roman_Katakana","strmif/DVD_CharSet_Unicode","strmif/DVD_TextCharSet"]
old-location: dshow\dvd_textcharset.htm
tech.root: dshow
ms.assetid: ee7d09e1-6274-4993-914e-d8f5efeb5f90
ms.date: 4/26/2023
ms.keywords: DVD_CharSet_ISO646, DVD_CharSet_ISO8859_1, DVD_CharSet_JIS_Roman_Kanji, DVD_CharSet_ShiftJIS_Kanji_Roman_Katakana, DVD_CharSet_Unicode, DVD_TextCharSet, DVD_TextCharSet , DVD_TextCharSet enumeration [DirectShow], DVD_TextCharSetEnumeration, dshow.dvd_textcharset, strmif/DVD_CharSet_ISO646, strmif/DVD_CharSet_ISO8859_1, strmif/DVD_CharSet_JIS_Roman_Kanji, strmif/DVD_CharSet_ShiftJIS_Kanji_Roman_Katakana, strmif/DVD_CharSet_Unicode, strmif/DVD_TextCharSet
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
 - DVD_TextCharSet
 - strmif/DVD_TextCharSet
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - DVD_TextCharSet
---

# DVD_TextCharSet enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Defines which character set a specified string is encoded with.

## -enum-fields

### -field DVD_CharSet_Unicode:0

Unicode character set.

### -field DVD_CharSet_ISO646:1

ISO 646 character set.

### -field DVD_CharSet_JIS_Roman_Kanji:2

Japanese Industrial Standards (JIS) Roman Kanji character set.

### -field DVD_CharSet_ISO8859_1:3

ISO 8859-1 character set.

### -field DVD_CharSet_ShiftJIS_Kanji_Roman_Katakana:4

JIS Kanji-Roman-Katakana character set.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo">IDvdInfo2::GetDVDTextLanguageInfo</a>
