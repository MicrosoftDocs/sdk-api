---
UID: NE:mi._MI_LocaleType
title: MI_LocaleType (mi.h)
description: Type of locale is needed when setting and getting locales.
helpviewer_keywords: ["MI_LOCALE_TYPE_CLOSEST_DATA","MI_LOCALE_TYPE_CLOSEST_UI","MI_LOCALE_TYPE_REQUESTED_DATA","MI_LOCALE_TYPE_REQUESTED_UI","MI_LocaleType","MI_LocaleType enumeration [Windows Management Infrastructure (MI)]","mi/MI_LOCALE_TYPE_CLOSEST_DATA","mi/MI_LOCALE_TYPE_CLOSEST_UI","mi/MI_LOCALE_TYPE_REQUESTED_DATA","mi/MI_LOCALE_TYPE_REQUESTED_UI","mi/MI_LocaleType","wmi._mi_localetype","wmi_v2.mi_localetype"]
old-location: wmi_v2\mi_localetype.htm
tech.root: wmi_v2
ms.assetid: e7a57fc1-a5a2-4c7f-9223-19adfb420237
ms.date: 12/05/2018
ms.keywords: MI_LOCALE_TYPE_CLOSEST_DATA, MI_LOCALE_TYPE_CLOSEST_UI, MI_LOCALE_TYPE_REQUESTED_DATA, MI_LOCALE_TYPE_REQUESTED_UI, MI_LocaleType, MI_LocaleType enumeration [Windows Management Infrastructure (MI)], mi/MI_LOCALE_TYPE_CLOSEST_DATA, mi/MI_LOCALE_TYPE_CLOSEST_UI, mi/MI_LOCALE_TYPE_REQUESTED_DATA, mi/MI_LOCALE_TYPE_REQUESTED_UI, mi/MI_LocaleType, wmi._mi_localetype, wmi_v2.mi_localetype
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
req.typenames: MI_LocaleType
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_LocaleType
 - mi/_MI_LocaleType
 - MI_LocaleType
 - mi/MI_LocaleType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_LocaleType
---

# MI_LocaleType enumeration


## -description

Type of locale is needed when setting and getting locales.

## -enum-fields

### -field MI_LOCALE_TYPE_REQUESTED_UI

The preferred language of error messages and dialog boxes.

### -field MI_LOCALE_TYPE_REQUESTED_DATA

The preferred date/time formats and  whether a comma or a decimal point is used in a floating-point number.

### -field MI_LOCALE_TYPE_CLOSEST_UI

The fallback error messages language if the requested language is not available.

### -field MI_LOCALE_TYPE_CLOSEST_DATA

The fallback data format if the requested language is not available.

