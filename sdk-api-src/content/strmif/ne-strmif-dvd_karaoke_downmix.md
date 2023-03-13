---
UID: NE:strmif.tagDVD_KARAOKE_DOWNMIX
title: DVD_KARAOKE_DOWNMIX (strmif.h)
description: Defines flags used by the IDvdControl2::SelectKaraokeAudioPresentationMode method to control which speakers, if any, each auxiliary channel is downmixed to.
helpviewer_keywords: ["DVD_KARAOKE_DOWNMIX","DVD_KARAOKE_DOWNMIX","DVD_KARAOKE_DOWNMIX enumeration [DirectShow]","DVD_KARAOKE_DOWNMIXEnumeration","DVD_Mix_0to0","DVD_Mix_0to1","DVD_Mix_1to0","DVD_Mix_1to1","DVD_Mix_2to0","DVD_Mix_2to1","DVD_Mix_3to0","DVD_Mix_3to1","DVD_Mix_4to0","DVD_Mix_4to1","DVD_Mix_Lto0","DVD_Mix_Lto1","DVD_Mix_Rto0","DVD_Mix_Rto1","dshow.dvd_karaoke_downmix","strmif/DVD_KARAOKE_DOWNMIX","strmif/DVD_Mix_0to0","strmif/DVD_Mix_0to1","strmif/DVD_Mix_1to0","strmif/DVD_Mix_1to1","strmif/DVD_Mix_2to0","strmif/DVD_Mix_2to1","strmif/DVD_Mix_3to0","strmif/DVD_Mix_3to1","strmif/DVD_Mix_4to0","strmif/DVD_Mix_4to1","strmif/DVD_Mix_Lto0","strmif/DVD_Mix_Lto1","strmif/DVD_Mix_Rto0","strmif/DVD_Mix_Rto1"]
old-location: dshow\dvd_karaoke_downmix.htm
tech.root: dshow
ms.assetid: 7f0132ae-6a46-4b81-9c5b-a0399a429b1a
ms.date: 12/05/2018
ms.keywords: DVD_KARAOKE_DOWNMIX, DVD_KARAOKE_DOWNMIX , DVD_KARAOKE_DOWNMIX enumeration [DirectShow], DVD_KARAOKE_DOWNMIXEnumeration, DVD_Mix_0to0, DVD_Mix_0to1, DVD_Mix_1to0, DVD_Mix_1to1, DVD_Mix_2to0, DVD_Mix_2to1, DVD_Mix_3to0, DVD_Mix_3to1, DVD_Mix_4to0, DVD_Mix_4to1, DVD_Mix_Lto0, DVD_Mix_Lto1, DVD_Mix_Rto0, DVD_Mix_Rto1, dshow.dvd_karaoke_downmix, strmif/DVD_KARAOKE_DOWNMIX, strmif/DVD_Mix_0to0, strmif/DVD_Mix_0to1, strmif/DVD_Mix_1to0, strmif/DVD_Mix_1to1, strmif/DVD_Mix_2to0, strmif/DVD_Mix_2to1, strmif/DVD_Mix_3to0, strmif/DVD_Mix_3to1, strmif/DVD_Mix_4to0, strmif/DVD_Mix_4to1, strmif/DVD_Mix_Lto0, strmif/DVD_Mix_Lto1, strmif/DVD_Mix_Rto0, strmif/DVD_Mix_Rto1
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
req.typenames: DVD_KARAOKE_DOWNMIX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDVD_KARAOKE_DOWNMIX
 - strmif/tagDVD_KARAOKE_DOWNMIX
 - DVD_KARAOKE_DOWNMIX
 - strmif/DVD_KARAOKE_DOWNMIX
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
 - DVD_KARAOKE_DOWNMIX
---

# DVD_KARAOKE_DOWNMIX enumeration


## -description

Defines flags used by the <a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-selectkaraokeaudiopresentationmode">IDvdControl2::SelectKaraokeAudioPresentationMode</a> method to control which speakers, if any, each auxiliary channel is downmixed to.

## -enum-fields

### -field DVD_Mix_0to0:0x1

Reserved.

### -field DVD_Mix_1to0:0x2

Reserved.

### -field DVD_Mix_2to0:0x4

Downmix channel 2 to the left speaker.

### -field DVD_Mix_3to0:0x8

Downmix channel 3 to the left speaker.

### -field DVD_Mix_4to0:0x10

Downmix channel 4 to the left speaker.

### -field DVD_Mix_Lto0:0x20

Reserved.

### -field DVD_Mix_Rto0:0x40

Reserved.

### -field DVD_Mix_0to1:0x100

Reserved.

### -field DVD_Mix_1to1:0x200

Reserved.

### -field DVD_Mix_2to1:0x400

Downmix channel 2 to the right speaker.

### -field DVD_Mix_3to1:0x800

Downmix channel 3 to the right speaker.

### -field DVD_Mix_4to1:0x1000

Downmix channel 4 to the right speaker.

### -field DVD_Mix_Lto1:0x2000

Reserved.

### -field DVD_Mix_Rto1:0x4000

Reserved.

## -remarks

Audio channels are zero-based, so channels 2 through 4 are the three auxiliary karaoke channels. Use bitwise <b>OR</b> operations to set the appropriate bit to send a channel to the left speaker (0), right speaker (1), both speakers, or to no speakers by turning both bits off. These bits are all off by default whenever the <a href="/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator Filter</a> filter enters karaoke mode.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-selectkaraokeaudiopresentationmode">IDvdControl2::SelectKaraokeAudioPresentationMode</a>
