---
UID: NE:mfidl._MFCLOCK_STATE
title: MFCLOCK_STATE (mfidl.h)
description: Defines the state of a clock.
helpviewer_keywords: ["90e04807-c3be-4f38-a508-9dfe62700869","MFCLOCK_STATE","MFCLOCK_STATE enumeration [Media Foundation]","MFCLOCK_STATE_INVALID","MFCLOCK_STATE_PAUSED","MFCLOCK_STATE_RUNNING","MFCLOCK_STATE_STOPPED","MF_CLOCK_STATE","MF_CLOCK_STATE enumeration [Media Foundation]","mf.mfclock_state","mfidl/MFCLOCK_STATE","mfidl/MFCLOCK_STATE_INVALID","mfidl/MFCLOCK_STATE_PAUSED","mfidl/MFCLOCK_STATE_RUNNING","mfidl/MFCLOCK_STATE_STOPPED"]
old-location: mf\mfclock_state.htm
tech.root: mf
ms.assetid: 90e04807-c3be-4f38-a508-9dfe62700869
ms.date: 12/05/2018
ms.keywords: 90e04807-c3be-4f38-a508-9dfe62700869, MFCLOCK_STATE, MFCLOCK_STATE enumeration [Media Foundation], MFCLOCK_STATE_INVALID, MFCLOCK_STATE_PAUSED, MFCLOCK_STATE_RUNNING, MFCLOCK_STATE_STOPPED, MF_CLOCK_STATE, MF_CLOCK_STATE enumeration [Media Foundation], mf.mfclock_state, mfidl/MFCLOCK_STATE, mfidl/MFCLOCK_STATE_INVALID, mfidl/MFCLOCK_STATE_PAUSED, mfidl/MFCLOCK_STATE_RUNNING, mfidl/MFCLOCK_STATE_STOPPED
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
req.typenames: MFCLOCK_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFCLOCK_STATE
 - mfidl/_MFCLOCK_STATE
 - MFCLOCK_STATE
 - mfidl/MFCLOCK_STATE
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
 - MF_CLOCK_STATE
---

# MFCLOCK_STATE enumeration


## -description

Defines the state of a clock.

## -enum-fields

### -field MFCLOCK_STATE_INVALID:0

The clock is invalid. A clock might be invalid for several reasons. Some clocks return this state before the first start. This state can also occur if the underlying device is lost.

### -field MFCLOCK_STATE_RUNNING

The clock is running. While the clock is running, the time advances at the clock's frequency and current rate.

### -field MFCLOCK_STATE_STOPPED

The clock is stopped. While stopped, the clock reports a time of 0.

### -field MFCLOCK_STATE_PAUSED

The clock is paused. While paused, the clock reports the time it was paused.

## -see-also

<a href="/windows/desktop/api/mfidl/nf-mfidl-imfclock-getstate">IMFClock::GetState</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
