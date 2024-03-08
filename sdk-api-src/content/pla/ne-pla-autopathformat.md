---
UID: NE:pla.__MIDL___MIDL_itf_pla_0001_0043_0003
title: AutoPathFormat (pla.h)
description: Defines how to decorate the file name or subdirectory name.
helpviewer_keywords: ["AutoPathFormat","AutoPathFormat enumeration [PLA]","base.autopathformat","pla.autopathformat","pla/AutoPathFormat","pla/plaComputer","pla/plaMonthDayHour","pla/plaMonthDayHourMinute","pla/plaNone","pla/plaPattern","pla/plaSerialNumber","pla/plaYearDayOfYear","pla/plaYearMonth","pla/plaYearMonthDay","pla/plaYearMonthDayHour","plaComputer","plaMonthDayHour","plaMonthDayHourMinute","plaNone","plaPattern","plaSerialNumber","plaYearDayOfYear","plaYearMonth","plaYearMonthDay","plaYearMonthDayHour"]
old-location: pla\autopathformat.htm
tech.root: PLA
ms.assetid: eee5e4fc-7754-44ad-b22d-5296223e2e9c
ms.date: 12/05/2018
ms.keywords: AutoPathFormat, AutoPathFormat enumeration [PLA], base.autopathformat, pla.autopathformat, pla/AutoPathFormat, pla/plaComputer, pla/plaMonthDayHour, pla/plaMonthDayHourMinute, pla/plaNone, pla/plaPattern, pla/plaSerialNumber, pla/plaYearDayOfYear, pla/plaYearMonth, pla/plaYearMonthDay, pla/plaYearMonthDayHour, plaComputer, plaMonthDayHour, plaMonthDayHourMinute, plaNone, plaPattern, plaSerialNumber, plaYearDayOfYear, plaYearMonth, plaYearMonthDay, plaYearMonthDayHour
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
req.typenames: AutoPathFormat
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_pla_0001_0043_0003
 - pla/__MIDL___MIDL_itf_pla_0001_0043_0003
 - AutoPathFormat
 - pla/AutoPathFormat
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
 - AutoPathFormat
---

# AutoPathFormat enumeration


## -description

Defines how to decorate the file name or subdirectory name.

## -enum-fields

### -field plaNone:0

Do not decorate the name.

### -field plaPattern:0x1

Add a pattern to the name. The pattern is specified in  the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_filenameformatpattern">IDataCollector::FileNameFormatPattern</a> or <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_subdirectoryformatpattern">IDataCollectorSet::SubdirectoryFormatPattern</a> property.

### -field plaComputer:0x2

Prefix the name with the computer name.

### -field plaMonthDayHour:0x100

Append the month, day, and hour to the name, in the form MMddHH.

### -field plaSerialNumber:0x200

Append the serial number specified in the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_serialnumber">IDataCollectorSet::SerialNumber</a> property to the subdirectory name in the form NNNNNN.

### -field plaYearDayOfYear:0x400

Append the year and day of the year to the name, in the form yyyyDDD.

### -field plaYearMonth:0x800

Append the year and month to the name, in the form yyyyMM.

### -field plaYearMonthDay:0x1000

Append the year, month, and day to the name, in the form yyyyMMdd.

### -field plaYearMonthDayHour:0x2000

Append the year, month, day, and hour to the name, in the form yyyyMMddHH.

### -field plaMonthDayHourMinute:0x4000

Append the month, day, hour, and minute to the name, in the form MMddHHmm.

## -remarks

Patterns apply to files and subdirectories in the same way.

For details on patterns, see the Remarks section of <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_filenameformatpattern">FileNameFormatPattern</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_filenameformat">IDataCollector::FileNameFormat</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_subdirectoryformat">IDataCollectorSet::SubdirectoryFormat</a>
