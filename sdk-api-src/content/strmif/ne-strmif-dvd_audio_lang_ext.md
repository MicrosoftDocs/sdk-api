---
UID: NE:strmif.tagDVD_AUDIO_LANG_EXT
title: DVD_AUDIO_LANG_EXT (strmif.h)
description: Defines flags that indicate whether an audio stream contains audio language extensions.
helpviewer_keywords: ["DVD_AUDIO_LANG_EXT","DVD_AUDIO_LANG_EXT","DVD_AUDIO_LANG_EXT enumeration [DirectShow]","DVD_AUDIO_LANG_EXTEnumeration","DVD_AUD_EXT_Captions","DVD_AUD_EXT_DirectorComments1","DVD_AUD_EXT_DirectorComments2","DVD_AUD_EXT_NotSpecified","DVD_AUD_EXT_VisuallyImpaired","dshow.dvd_audio_lang_ext","strmif/DVD_AUDIO_LANG_EXT","strmif/DVD_AUD_EXT_Captions","strmif/DVD_AUD_EXT_DirectorComments1","strmif/DVD_AUD_EXT_DirectorComments2","strmif/DVD_AUD_EXT_NotSpecified","strmif/DVD_AUD_EXT_VisuallyImpaired"]
old-location: dshow\dvd_audio_lang_ext.htm
tech.root: dshow
ms.assetid: 01d82199-18e1-4d84-add1-f4f6790155c8
ms.date: 12/05/2018
ms.keywords: DVD_AUDIO_LANG_EXT, DVD_AUDIO_LANG_EXT , DVD_AUDIO_LANG_EXT enumeration [DirectShow], DVD_AUDIO_LANG_EXTEnumeration, DVD_AUD_EXT_Captions, DVD_AUD_EXT_DirectorComments1, DVD_AUD_EXT_DirectorComments2, DVD_AUD_EXT_NotSpecified, DVD_AUD_EXT_VisuallyImpaired, dshow.dvd_audio_lang_ext, strmif/DVD_AUDIO_LANG_EXT, strmif/DVD_AUD_EXT_Captions, strmif/DVD_AUD_EXT_DirectorComments1, strmif/DVD_AUD_EXT_DirectorComments2, strmif/DVD_AUD_EXT_NotSpecified, strmif/DVD_AUD_EXT_VisuallyImpaired
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
req.typenames: DVD_AUDIO_LANG_EXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDVD_AUDIO_LANG_EXT
 - strmif/tagDVD_AUDIO_LANG_EXT
 - DVD_AUDIO_LANG_EXT
 - strmif/DVD_AUDIO_LANG_EXT
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
 - DVD_AUDIO_LANG_EXT
---

# DVD_AUDIO_LANG_EXT enumeration


## -description

Defines flags that indicate whether an audio stream contains audio language extensions.

## -enum-fields

### -field DVD_AUD_EXT_NotSpecified:0

The DVD doesn't specify an audio language extension for this audio stream.

### -field DVD_AUD_EXT_Captions:1

The audio stream contains captions.

### -field DVD_AUD_EXT_VisuallyImpaired:2

The audio stream contains content for people with low vision.

### -field DVD_AUD_EXT_DirectorComments1:3

The audio stream contains "director comments 1."

### -field DVD_AUD_EXT_DirectorComments2:4

The audio stream contains "director comments 2."

## -remarks

This enumeration is used in the <a href="/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getaudioattributes">IDvdInfo2::GetAudioAttributes</a> and <a href="/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getdefaultaudiolanguage">IDvdInfo2::GetDefaultAudioLanguage</a> methods.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2</a>
