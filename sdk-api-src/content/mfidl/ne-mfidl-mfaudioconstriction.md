---
UID: NE:mfidl._MFAudioConstriction
title: MFAudioConstriction (mfidl.h)
description: Specifies values for audio constriction.
helpviewer_keywords: ["MFAudioConstriction","MFAudioConstriction enumeration [Media Foundation]","MFaudioConstriction14_14","MFaudioConstriction44_16","MFaudioConstriction48_16","MFaudioConstrictionMute","MFaudioConstrictionOff","mf.mfaudioconstriction","mfidl/MFAudioConstriction","mfidl/MFaudioConstriction14_14","mfidl/MFaudioConstriction44_16","mfidl/MFaudioConstriction48_16","mfidl/MFaudioConstrictionMute","mfidl/MFaudioConstrictionOff"]
old-location: mf\mfaudioconstriction.htm
tech.root: mf
ms.assetid: EAFE3AA5-EF63-471A-9A67-A2EB298B0C0F
ms.date: 12/05/2018
ms.keywords: MFAudioConstriction, MFAudioConstriction enumeration [Media Foundation], MFaudioConstriction14_14, MFaudioConstriction44_16, MFaudioConstriction48_16, MFaudioConstrictionMute, MFaudioConstrictionOff, mf.mfaudioconstriction, mfidl/MFAudioConstriction, mfidl/MFaudioConstriction14_14, mfidl/MFaudioConstriction44_16, mfidl/MFaudioConstriction48_16, mfidl/MFaudioConstrictionMute, mfidl/MFaudioConstrictionOff
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.typenames: MFAudioConstriction
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFAudioConstriction
 - mfidl/_MFAudioConstriction
 - MFAudioConstriction
 - mfidl/MFAudioConstriction
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
 - MFAudioConstriction
---

# MFAudioConstriction enumeration


## -description

Specifies values for audio constriction.

## -enum-fields

### -field MFaudioConstrictionOff:0

Audio is not constricted.

### -field MFaudioConstriction48_16

Audio is down sampled to 48 kHz/16-bit.

### -field MFaudioConstriction44_16

Audio is down sampled to 44 kHz/16-bit.

### -field MFaudioConstriction14_14

Audio is down sampled to 14hKz/16-bit.

### -field MFaudioConstrictionMute

Audio is muted.

## -remarks

Values defined by the <b>MFAudioConstriction</b> enumeration matches the <b>EAudioConstriction</b> enumeration defined <b>audioenginebaseapo.h</b>.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
