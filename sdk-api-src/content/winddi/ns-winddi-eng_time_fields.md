---
UID: NS:winddi._ENG_TIME_FIELDS
title: ENG_TIME_FIELDS (winddi.h)
description: The ENG_TIME_FIELDS structure is used by the EngQueryLocalTime function to return the local time.
helpviewer_keywords: ["*PENG_TIME_FIELDS","ENG_TIME_FIELDS","ENG_TIME_FIELDS structure [Display Devices]","PENG_TIME_FIELDS","PENG_TIME_FIELDS structure pointer [Display Devices]","display.eng_time_fields","grstrcts_3611274f-4217-48c5-af9d-9470df8a39e8.xml","winddi/ENG_TIME_FIELDS","winddi/PENG_TIME_FIELDS"]
old-location: display\eng_time_fields.htm
tech.root: display
ms.assetid: 482e1d15-d499-4ed2-87e7-760f03a454b5
ms.date: 12/05/2018
ms.keywords: '*PENG_TIME_FIELDS, ENG_TIME_FIELDS, ENG_TIME_FIELDS structure [Display Devices], PENG_TIME_FIELDS, PENG_TIME_FIELDS structure pointer [Display Devices], display.eng_time_fields, grstrcts_3611274f-4217-48c5-af9d-9470df8a39e8.xml, winddi/ENG_TIME_FIELDS, winddi/PENG_TIME_FIELDS'
req.header: winddi.h
req.include-header: Winddi.h
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
req.typenames: ENG_TIME_FIELDS, *PENG_TIME_FIELDS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ENG_TIME_FIELDS
 - winddi/_ENG_TIME_FIELDS
 - PENG_TIME_FIELDS
 - winddi/PENG_TIME_FIELDS
 - ENG_TIME_FIELDS
 - winddi/ENG_TIME_FIELDS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - ENG_TIME_FIELDS
---

# ENG_TIME_FIELDS structure


## -description

The ENG_TIME_FIELDS structure is used by the  <a href="/windows/desktop/api/winddi/nf-winddi-engquerylocaltime">EngQueryLocalTime</a> function to return the local time.

## -struct-fields

### -field usYear

Specifies the current calendar year. The range is [1601,...].

### -field usMonth

Specifies the current calendar month. The range is [1,12].

### -field usDay

Specifies the current calendar day. The range is [1,31].

### -field usHour

Specifies the current hour. The range is [0,23].

### -field usMinute

Specifies the current minute. The range is [0,59].

### -field usSecond

Specifies the current second. The range is [0,59].

### -field usMilliseconds

Specifies the current millisecond. The range is [0,999].

### -field usWeekday

Specifies the current day. The range is [0,6], where 0 is Sunday and 6 is Saturday.

## -remarks

The driver is responsible for allocating the ENG_TIME_FIELDS structure and passing its pointer to <b>EngQueryLocalTime</b>.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engquerylocaltime">EngQueryLocalTime</a>