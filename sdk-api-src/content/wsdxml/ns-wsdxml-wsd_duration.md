---
UID: NS:wsdxml._WSD_DURATION
title: WSD_DURATION (wsdxml.h)
description: Represents a length of time.
helpviewer_keywords: ["WSD_DURATION","WSD_DURATION structure","_WSD_DURATION","ncd.wsd_duration_struct","wsdxml/WSD_DURATION"]
old-location: ncd\wsd_duration_struct.htm
tech.root: ncd
ms.assetid: 43d4d0c5-509a-46c4-bdf6-24c3307fb811
ms.date: 12/05/2018
ms.keywords: WSD_DURATION, WSD_DURATION structure, _WSD_DURATION, ncd.wsd_duration_struct, wsdxml/WSD_DURATION
req.header: wsdxml.h
req.include-header: Wsdapi.h
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
req.typenames: WSD_DURATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSD_DURATION
 - wsdxml/_WSD_DURATION
 - WSD_DURATION
 - wsdxml/WSD_DURATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WsdXml.h
api_name:
 - WSD_DURATION
---

# WSD_DURATION structure


## -description

Represents a length of time.

## -struct-fields

### -field isPositive

This parameter is <b>TRUE</b> if the entire duration is positive.

### -field year

The year value. This number is a value between 0 and max(ULONG).

### -field month

The month value. This number is a value between 0 and max(ULONG).

### -field day

The day value. This number is a value between 0 and max(ULONG).

### -field hour

The hour value. This number is a value between 0 and max(ULONG).

### -field minute

The minute value. This number is a value between 0 and max(ULONG).

### -field second

The second value. This number is a value between 0 and max(ULONG).

### -field millisecond

The millisecond value (0-999).

## -remarks

If any numeric member has a value of 0, then the member and its value is not included in the XML output when the structure is converted to XML.

