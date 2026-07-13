---
UID: NE:mfidl._MFCLOCK_CHARACTERISTICS_FLAGS
title: MFCLOCK_CHARACTERISTICS_FLAGS (mfidl.h)
description: Contains flags that describe the characteristics of a clock.
helpviewer_keywords: ["8064ce25-6c79-479b-a1a8-bdcc2c29ad54","MFCLOCK_CHARACTERISTICS_FLAGS","MFCLOCK_CHARACTERISTICS_FLAGS enumeration [Media Foundation]","MFCLOCK_CHARACTERISTICS_FLAG_ALWAYS_RUNNING","MFCLOCK_CHARACTERISTICS_FLAG_FREQUENCY_10MHZ","MFCLOCK_CHARACTERISTICS_FLAG_IS_SYSTEM_CLOCK","enumeration [Media Foundation]","mf.mfclock_characteristics_flags","mfidl/MFCLOCK_CHARACTERISTICS_FLAGS","mfidl/MFCLOCK_CHARACTERISTICS_FLAG_ALWAYS_RUNNING","mfidl/MFCLOCK_CHARACTERISTICS_FLAG_FREQUENCY_10MHZ","mfidl/MFCLOCK_CHARACTERISTICS_FLAG_IS_SYSTEM_CLOCK"]
old-location: mf\mfclock_characteristics_flags.htm
tech.root: mf
ms.assetid: 8064ce25-6c79-479b-a1a8-bdcc2c29ad54
ms.date: 12/05/2018
ms.keywords: 8064ce25-6c79-479b-a1a8-bdcc2c29ad54, MFCLOCK_CHARACTERISTICS_FLAGS, MFCLOCK_CHARACTERISTICS_FLAGS enumeration [Media Foundation], MFCLOCK_CHARACTERISTICS_FLAG_ALWAYS_RUNNING, MFCLOCK_CHARACTERISTICS_FLAG_FREQUENCY_10MHZ, MFCLOCK_CHARACTERISTICS_FLAG_IS_SYSTEM_CLOCK, enumeration [Media Foundation], mf.mfclock_characteristics_flags, mfidl/MFCLOCK_CHARACTERISTICS_FLAGS, mfidl/MFCLOCK_CHARACTERISTICS_FLAG_ALWAYS_RUNNING, mfidl/MFCLOCK_CHARACTERISTICS_FLAG_FREQUENCY_10MHZ, mfidl/MFCLOCK_CHARACTERISTICS_FLAG_IS_SYSTEM_CLOCK
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
req.typenames: MFCLOCK_CHARACTERISTICS_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFCLOCK_CHARACTERISTICS_FLAGS
 - mfidl/_MFCLOCK_CHARACTERISTICS_FLAGS
 - MFCLOCK_CHARACTERISTICS_FLAGS
 - mfidl/MFCLOCK_CHARACTERISTICS_FLAGS
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
 - MFCLOCK_CHARACTERISTICS_FLAGS
---

# MFCLOCK_CHARACTERISTICS_FLAGS enumeration


## -description

Contains flags that describe the characteristics of a clock. These flags are returned by the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclock-getclockcharacteristics">IMFClock::GetClockCharacteristics</a> method.

## -enum-fields

### -field MFCLOCK_CHARACTERISTICS_FLAG_FREQUENCY_10MHZ:0x2

The clock times returned by the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime">IMFClock::GetCorrelatedTime</a> method are in units of 100 nanoseconds. If this flag is absent, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclock-getproperties">IMFClock::GetProperties</a> to get the clock frequency. The clock frequency is given in the <b>qwClockFrequency</b> member of the <a href="/windows/desktop/api/mfidl/ns-mfidl-mfclock_properties">MFCLOCK_PROPERTIES</a> structure returned by that method.

### -field MFCLOCK_CHARACTERISTICS_FLAG_ALWAYS_RUNNING:0x4

The clock is always running. If this flag is present, the clock cannot be paused or stopped. If this flag is absent, call the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclock-getstate">IMFClock::GetState</a> method to get the current state.

### -field MFCLOCK_CHARACTERISTICS_FLAG_IS_SYSTEM_CLOCK:0x8

The clock times are generated from the system clock.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
