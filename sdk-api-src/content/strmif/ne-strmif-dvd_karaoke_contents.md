---
UID: NE:strmif.tagDVD_KARAOKE_CONTENTS
title: DVD_KARAOKE_CONTENTS (strmif.h)
description: Specifies flags that, when used in a bitwise OR operation, describe the contents of each channel of an audio stream in a karaoke title.
helpviewer_keywords: ["DVD_KARAOKE_CONTENTS","DVD_KARAOKE_CONTENTS","DVD_KARAOKE_CONTENTS enumeration [DirectShow]","DVD_KARAOKE_CONTENTSEnumeration","DVD_Karaoke_GuideMelody1","DVD_Karaoke_GuideMelody2","DVD_Karaoke_GuideMelodyA","DVD_Karaoke_GuideMelodyB","DVD_Karaoke_GuideVocal1","DVD_Karaoke_GuideVocal2","DVD_Karaoke_SoundEffectA","DVD_Karaoke_SoundEffectB","dshow.dvd_karaoke_contents","strmif/DVD_KARAOKE_CONTENTS","strmif/DVD_Karaoke_GuideMelody1","strmif/DVD_Karaoke_GuideMelody2","strmif/DVD_Karaoke_GuideMelodyA","strmif/DVD_Karaoke_GuideMelodyB","strmif/DVD_Karaoke_GuideVocal1","strmif/DVD_Karaoke_GuideVocal2","strmif/DVD_Karaoke_SoundEffectA","strmif/DVD_Karaoke_SoundEffectB"]
old-location: dshow\dvd_karaoke_contents.htm
tech.root: dshow
ms.assetid: 9d02b0bf-237a-42bf-b946-588b899cd3d9
ms.date: 12/05/2018
ms.keywords: DVD_KARAOKE_CONTENTS, DVD_KARAOKE_CONTENTS , DVD_KARAOKE_CONTENTS enumeration [DirectShow], DVD_KARAOKE_CONTENTSEnumeration, DVD_Karaoke_GuideMelody1, DVD_Karaoke_GuideMelody2, DVD_Karaoke_GuideMelodyA, DVD_Karaoke_GuideMelodyB, DVD_Karaoke_GuideVocal1, DVD_Karaoke_GuideVocal2, DVD_Karaoke_SoundEffectA, DVD_Karaoke_SoundEffectB, dshow.dvd_karaoke_contents, strmif/DVD_KARAOKE_CONTENTS, strmif/DVD_Karaoke_GuideMelody1, strmif/DVD_Karaoke_GuideMelody2, strmif/DVD_Karaoke_GuideMelodyA, strmif/DVD_Karaoke_GuideMelodyB, strmif/DVD_Karaoke_GuideVocal1, strmif/DVD_Karaoke_GuideVocal2, strmif/DVD_Karaoke_SoundEffectA, strmif/DVD_Karaoke_SoundEffectB
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
req.typenames: DVD_KARAOKE_CONTENTS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDVD_KARAOKE_CONTENTS
 - strmif/tagDVD_KARAOKE_CONTENTS
 - DVD_KARAOKE_CONTENTS
 - strmif/DVD_KARAOKE_CONTENTS
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
 - DVD_KARAOKE_CONTENTS
---

# DVD_KARAOKE_CONTENTS enumeration


## -description

Specifies flags that, when used in a bitwise <b>OR</b> operation, describe the contents of each channel of an audio stream in a karaoke title.

## -enum-fields

### -field DVD_Karaoke_GuideVocal1:0x1

The channel contains guide vocal 1.

### -field DVD_Karaoke_GuideVocal2:0x2

The channel contains guide vocal 2.

### -field DVD_Karaoke_GuideMelody1:0x4

The channel contains guide melody 1.

### -field DVD_Karaoke_GuideMelody2:0x8

The channel contains guide melody 2.

### -field DVD_Karaoke_GuideMelodyA:0x10

The channel contains guide melody A.

### -field DVD_Karaoke_GuideMelodyB:0x20

The channel contains guide melody B.

### -field DVD_Karaoke_SoundEffectA:0x40

The channel contains sound effect A.

### -field DVD_Karaoke_SoundEffectB:0x80

The channel contains sound effect B.

## -remarks

This enumeration is used in the [DVD_KaraokeAttributes](/windows/desktop/api/strmif/ns-strmif-dvd_karaokeattributes) structure.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>
