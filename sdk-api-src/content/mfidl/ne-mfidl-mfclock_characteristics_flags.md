---
UID: NE:mfidl._MFCLOCK_CHARACTERISTICS_FLAGS
title: MFCLOCK_CHARACTERISTICS_FLAGS (mfidl.h)
author: windows-sdk-content
description: Contains flags that describe the characteristics of a clock.
old-location: mf\mfclock_characteristics_flags.htm
tech.root: medfound
ms.assetid: 8064ce25-6c79-479b-a1a8-bdcc2c29ad54
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 8064ce25-6c79-479b-a1a8-bdcc2c29ad54, MFCLOCK_CHARACTERISTICS_FLAGS, MFCLOCK_CHARACTERISTICS_FLAGS enumeration [Media Foundation], MFCLOCK_CHARACTERISTICS_FLAG_ALWAYS_RUNNING, MFCLOCK_CHARACTERISTICS_FLAG_FREQUENCY_10MHZ, MFCLOCK_CHARACTERISTICS_FLAG_IS_SYSTEM_CLOCK, enumeration [Media Foundation], mf.mfclock_characteristics_flags, mfidl/MFCLOCK_CHARACTERISTICS_FLAGS, mfidl/MFCLOCK_CHARACTERISTICS_FLAG_ALWAYS_RUNNING, mfidl/MFCLOCK_CHARACTERISTICS_FLAG_FREQUENCY_10MHZ, mfidl/MFCLOCK_CHARACTERISTICS_FLAG_IS_SYSTEM_CLOCK
ms.topic: enum
f1_keywords: ["mfidl/MFCLOCK_CHARACTERISTICS_FLAGS"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MFCLOCK_CHARACTERISTICS_FLAGS
product: Windows
targetos: Windows
req.typenames: MFCLOCK_CHARACTERISTICS_FLAGS
req.redist: 
ms.custom: 19H1
---

# MFCLOCK_CHARACTERISTICS_FLAGS enumeration


## -description


Contains flags that describe the characteristics of a clock. These flags are returned by the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfclock-getclockcharacteristics">IMFClock::GetClockCharacteristics</a> method.


## -enum-fields




### -field MFCLOCK_CHARACTERISTICS_FLAG_FREQUENCY_10MHZ

The clock times returned by the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime">IMFClock::GetCorrelatedTime</a> method are in units of 100 nanoseconds. If this flag is absent, call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfclock-getproperties">IMFClock::GetProperties</a> to get the clock frequency. The clock frequency is given in the <b>qwClockFrequency</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/ns-mfidl-_mfclock_properties">MFCLOCK_PROPERTIES</a> structure returned by that method.


### -field MFCLOCK_CHARACTERISTICS_FLAG_ALWAYS_RUNNING

The clock is always running. If this flag is present, the clock cannot be paused or stopped. If this flag is absent, call the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfclock-getstate">IMFClock::GetState</a> method to get the current state.


### -field MFCLOCK_CHARACTERISTICS_FLAG_IS_SYSTEM_CLOCK

The clock times are generated from the system clock.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
 

 

