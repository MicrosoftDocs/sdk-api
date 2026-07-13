---
UID: NE:mfidl._MFCLOCK_RELATIONAL_FLAGS
title: MFCLOCK_RELATIONAL_FLAGS (mfidl.h)
description: Defines properties of a clock.
helpviewer_keywords: ["MFCLOCK_RELATIONAL_FLAGS","MFCLOCK_RELATIONAL_FLAGS enumeration [Media Foundation]","MFCLOCK_RELATIONAL_FLAG_JITTER_NEVER_AHEAD","d70b432c-6ebd-405c-993f-12c4540736d7","mf.mfclock_relational_flags","mfidl/MFCLOCK_RELATIONAL_FLAGS","mfidl/MFCLOCK_RELATIONAL_FLAG_JITTER_NEVER_AHEAD"]
old-location: mf\mfclock_relational_flags.htm
tech.root: mf
ms.assetid: d70b432c-6ebd-405c-993f-12c4540736d7
ms.date: 12/05/2018
ms.keywords: MFCLOCK_RELATIONAL_FLAGS, MFCLOCK_RELATIONAL_FLAGS enumeration [Media Foundation], MFCLOCK_RELATIONAL_FLAG_JITTER_NEVER_AHEAD, d70b432c-6ebd-405c-993f-12c4540736d7, mf.mfclock_relational_flags, mfidl/MFCLOCK_RELATIONAL_FLAGS, mfidl/MFCLOCK_RELATIONAL_FLAG_JITTER_NEVER_AHEAD
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: MFCLOCK_RELATIONAL_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFCLOCK_RELATIONAL_FLAGS
 - mfidl/_MFCLOCK_RELATIONAL_FLAGS
 - MFCLOCK_RELATIONAL_FLAGS
 - mfidl/MFCLOCK_RELATIONAL_FLAGS
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
 - MFCLOCK_RELATIONAL_FLAGS
---

# MFCLOCK_RELATIONAL_FLAGS enumeration


## -description

Defines properties of a clock.

## -enum-fields

### -field MFCLOCK_RELATIONAL_FLAG_JITTER_NEVER_AHEAD:0x1

Jitter values are always negative. In other words, the time returned by <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime">IMFClock::GetCorrelatedTime</a> might jitter behind the actual clock time, but will never jitter ahead of the actual time. If this flag is not present, the clock might jitter in either direction.

## -see-also

<a href="/windows/desktop/api/mfidl/ns-mfidl-mfclock_properties">MFCLOCK_PROPERTIES</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
