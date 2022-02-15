---
UID: NE:pla.__MIDL___MIDL_itf_pla_0001_0043_0009
title: WeekDays (pla.h)
description: Defines the days of the week on which to run the data collector set.
helpviewer_keywords: ["WeekDays","WeekDays enumeration [PLA]","base.weekdays","pla.weekdays","pla/WeekDays","pla/plaEveryday","pla/plaFriday","pla/plaMonday","pla/plaRunOnce","pla/plaSaturday","pla/plaSunday","pla/plaThursday","pla/plaTuesday","pla/plaWednesday","plaEveryday","plaFriday","plaMonday","plaRunOnce","plaSaturday","plaSunday","plaThursday","plaTuesday","plaWednesday"]
old-location: pla\weekdays.htm
tech.root: PLA
ms.assetid: 5246fee3-0536-4525-bab8-5087330a1b49
ms.date: 12/05/2018
ms.keywords: WeekDays, WeekDays enumeration [PLA], base.weekdays, pla.weekdays, pla/WeekDays, pla/plaEveryday, pla/plaFriday, pla/plaMonday, pla/plaRunOnce, pla/plaSaturday, pla/plaSunday, pla/plaThursday, pla/plaTuesday, pla/plaWednesday, plaEveryday, plaFriday, plaMonday, plaRunOnce, plaSaturday, plaSunday, plaThursday, plaTuesday, plaWednesday
req.header: pla.h
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
req.typenames: WeekDays
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_pla_0001_0043_0009
 - pla/__MIDL___MIDL_itf_pla_0001_0043_0009
 - WeekDays
 - pla/WeekDays
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Pla.h
api_name:
 - WeekDays
---

# WeekDays enumeration


## -description

Defines the days of the week on which to run the data collector set.

## -enum-fields

### -field plaRunOnce:0

Run only once on the specified start date and time.

### -field plaSunday:0x1

Run on Sunday.

### -field plaMonday:0x2

Run on Monday.

### -field plaTuesday:0x4

Run on Tuesday.

### -field plaWednesday:0x8

Run on Wednesday

### -field plaThursday:0x10

Run on Thursday.

### -field plaFriday:0x20

Run on Friday.

### -field plaSaturday:0x40

Run on Saturday.

### -field plaEveryday:0x7f

Run every day of the week.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nf-pla-ischedule-get_days">ISchedule::Days</a>
