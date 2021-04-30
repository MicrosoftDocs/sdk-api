---
UID: NS:windows.foundation.DateTime
title: DateTime (windows.foundation.h)
description: Represents an instant in time, typically expressed as a date and time of day.
helpviewer_keywords: ["DateTime","DateTime structure [Windows Runtime]","windows/DateTime","winrt.datetime"]
old-location: winrt\datetime.htm
tech.root: WinRT
ms.assetid: b5533002-8a72-438d-a3d3-0902ffc21830
ms.date: 12/05/2018
ms.keywords: DateTime, DateTime structure [Windows Runtime], windows/DateTime, winrt.datetime
req.header: windows.foundation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Windows.Foundation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DateTime
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DateTime
 - windows.foundation/DateTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windows.Foundation.h
api_name:
 - DateTime
---

# DateTime structure


## -description

Represents an instant in time, typically expressed as a date and time of day.

## -struct-fields

### -field DateTime.UniversalTime

### -field UniversalTime

Type: <b>INT64</b>

The number of 100-nanosecond intervals that have elapsed since 12:00:00 midnight on January 1, 1601 CE, UTC time.

## -see-also

<a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvaluestatics-createdatetime">CreateDateTime</a>



<a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvaluestatics-createdatetimearray">CreateDateTimeArray</a>



<a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getdatetime">IPropertyValue::GetDateTime</a>



<a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getdatetimearray">IPropertyValue::GetDateTimeArray</a>