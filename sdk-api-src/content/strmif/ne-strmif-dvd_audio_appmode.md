---
UID: NE:strmif.tagDVD_AUDIO_APPMODE
title: DVD_AUDIO_APPMODE (strmif.h)
description: Indicates the current audio mode as retrieved in a call to IDvdInfo2::GetAudioAttributes.
helpviewer_keywords: ["DVD_AUDIO_APPMODE","DVD_AUDIO_APPMODE","DVD_AUDIO_APPMODE enumeration [DirectShow]","DVD_AUDIO_APPMODEEnumeration","DVD_AudioMode_Karaoke","DVD_AudioMode_None","DVD_AudioMode_Other","DVD_AudioMode_Surround","dshow.dvd_audio_appmode","strmif/DVD_AUDIO_APPMODE","strmif/DVD_AudioMode_Karaoke","strmif/DVD_AudioMode_None","strmif/DVD_AudioMode_Other","strmif/DVD_AudioMode_Surround"]
old-location: dshow\dvd_audio_appmode.htm
tech.root: dshow
ms.assetid: 900fd812-7ca0-4dd8-bb30-3c8eff136939
ms.date: 12/05/2018
ms.keywords: DVD_AUDIO_APPMODE, DVD_AUDIO_APPMODE , DVD_AUDIO_APPMODE enumeration [DirectShow], DVD_AUDIO_APPMODEEnumeration, DVD_AudioMode_Karaoke, DVD_AudioMode_None, DVD_AudioMode_Other, DVD_AudioMode_Surround, dshow.dvd_audio_appmode, strmif/DVD_AUDIO_APPMODE, strmif/DVD_AudioMode_Karaoke, strmif/DVD_AudioMode_None, strmif/DVD_AudioMode_Other, strmif/DVD_AudioMode_Surround
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
req.typenames: DVD_AUDIO_APPMODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDVD_AUDIO_APPMODE
 - strmif/tagDVD_AUDIO_APPMODE
 - DVD_AUDIO_APPMODE
 - strmif/DVD_AUDIO_APPMODE
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
 - DVD_AUDIO_APPMODE
---

# DVD_AUDIO_APPMODE enumeration


## -description

Indicates the current audio mode as retrieved in a call to <a href="/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getaudioattributes">IDvdInfo2::GetAudioAttributes</a>.

## -enum-fields

### -field DVD_AudioMode_None:0

No special audio mode. The <a href="/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator Filter</a> will send the audio to the decoder with no special processing.

### -field DVD_AudioMode_Karaoke:1

The current audio mode is karaoke content.

### -field DVD_AudioMode_Surround:2

The current audio mode is surround sound.

### -field DVD_AudioMode_Other:3

Unrecognized audio mode.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getaudioattributes">IDvdInfo2::GetAudioAttributes</a>
