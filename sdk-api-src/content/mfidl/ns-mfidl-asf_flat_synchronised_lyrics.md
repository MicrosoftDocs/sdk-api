---
UID: NS:mfidl._ASFFlatSynchronisedLyrics
title: ASF_FLAT_SYNCHRONISED_LYRICS (mfidl.h)
description: Contains synchronized lyrics stored as metadata for a media source. This structure is used as the data item for the WM/Lyrics_Synchronised metadata attribute.
helpviewer_keywords: ["518c7e81-6492-40f9-a8e8-222c19de6cc0","ASF_FLAT_SYNCHRONISED_LYRICS","ASF_FLAT_SYNCHRONISED_LYRICS structure [Media Foundation]","mf.asf_flat_synchronised_lyrics","mfidl/ASF_FLAT_SYNCHRONISED_LYRICS"]
old-location: mf\asf_flat_synchronised_lyrics.htm
tech.root: mf
ms.assetid: 518c7e81-6492-40f9-a8e8-222c19de6cc0
ms.date: 12/05/2018
ms.keywords: 518c7e81-6492-40f9-a8e8-222c19de6cc0, ASF_FLAT_SYNCHRONISED_LYRICS, ASF_FLAT_SYNCHRONISED_LYRICS structure [Media Foundation], mf.asf_flat_synchronised_lyrics, mfidl/ASF_FLAT_SYNCHRONISED_LYRICS
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: ASF_FLAT_SYNCHRONISED_LYRICS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ASFFlatSynchronisedLyrics
 - mfidl/_ASFFlatSynchronisedLyrics
 - ASF_FLAT_SYNCHRONISED_LYRICS
 - mfidl/ASF_FLAT_SYNCHRONISED_LYRICS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - ASF_FLAT_SYNCHRONISED_LYRICS
---

# ASF_FLAT_SYNCHRONISED_LYRICS structure


## -description

Contains synchronized lyrics stored as metadata for a media source. This structure is used as the data item for the <b>WM/Lyrics_Synchronised</b> metadata attribute.

## -struct-fields

### -field bTimeStampFormat

Specifies the format of time stamps in the lyrics. This member is equivalent to the <b>bTimeStampFormat</b> member in the <b>WM_SYNCHRONISED_LYRICS</b> structure. The <b>WM_SYNCHRONISED_LYRICS</b> structure is documented in the Windows Media Format SDK.

### -field bContentType

Specifies the type of synchronized strings that are in the lyric data. This member is equivalent to the <b>bContentType</b> member in the <b>WM_SYNCHRONISED_LYRICS</b> structure.

### -field dwLyricsLen

Size, in bytes, of the lyric data.

## -remarks

The <b>WM/Lyrics_Synchronised</b> attribute is defined in the Windows Media Format SDK. The attribute contains lyrics synchronized to times in the source file.

To get this attribute from a media source, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty">IMFMetadata::GetProperty</a>, passing in the constant g_wszWMLyrics_Synchronised for the <i>pwszName</i> parameter. The method retrieves a <b>PROPVARIANT</b> that contains a binary array (VT_BLOB). The layout of the array is as follows:

<ul>
<li>
<b>ASF_FLAT_SYNCHRONISED_LYRICS</b> structure.

</li>
<li>
Null-terminated wide-character string that contains a description.

</li>
<li>
Lyric data. The format of the lyric data is described in the Windows Media Format SDK documentation.

</li>
</ul>
This format differs from the <b>WM_SYNCHRONISED_LYRICS</b> structure used in the Windows Media Format SDK. The <b>WM_SYNCHRONISED_LYRICS</b> structure contains internal pointers to two strings and the lyric data. If the structure is copied, these pointers become invalid. The <b>ASF_FLAT_SYNCHRONISED_LYRICS</b> structure does not contain internal pointers, so it is safe to copy the structure.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadata">IMFMetadata</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>