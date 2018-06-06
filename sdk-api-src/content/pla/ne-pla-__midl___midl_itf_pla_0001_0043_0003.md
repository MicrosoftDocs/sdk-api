---
UID: NE:pla.__MIDL___MIDL_itf_pla_0001_0043_0003
title: "__MIDL___MIDL_itf_pla_0001_0043_0003"
author: windows-sdk-content
description: Defines how to decorate the file name or subdirectory name.
old-location: pla\autopathformat.htm
old-project: PLA
ms.assetid: eee5e4fc-7754-44ad-b22d-5296223e2e9c
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: AutoPathFormat, AutoPathFormat enumeration [PLA], __MIDL___MIDL_itf_pla_0001_0043_0003, base.autopathformat, pla.autopathformat, pla/AutoPathFormat, pla/plaComputer, pla/plaMonthDayHour, pla/plaMonthDayHourMinute, pla/plaNone, pla/plaPattern, pla/plaSerialNumber, pla/plaYearDayOfYear, pla/plaYearMonth, pla/plaYearMonthDay, pla/plaYearMonthDayHour, plaComputer, plaMonthDayHour, plaMonthDayHourMinute, plaNone, plaPattern, plaSerialNumber, plaYearDayOfYear, plaYearMonth, plaYearMonthDay, plaYearMonthDayHour
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: AutoPathFormat
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Pla.h
api_name:
 - AutoPathFormat
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# __MIDL___MIDL_itf_pla_0001_0043_0003 enumeration


## -description


Defines how to decorate the file name or subdirectory name.


## -enum-fields




### -field plaNone

Do not decorate the name.


### -field plaPattern

Add a pattern to the name. The pattern is specified in  the <a href="https://msdn.microsoft.com/94e6bb13-fb99-4968-8a7f-fbda1f6ea42e">IDataCollector::FileNameFormatPattern</a> or <a href="https://msdn.microsoft.com/83b7df10-8b00-4d64-bf71-2c68e037ab3f">IDataCollectorSet::SubdirectoryFormatPattern</a> property.


### -field plaComputer

Prefix the name with the computer name.


### -field plaMonthDayHour

Append the month, day, and hour to the name, in the form MMddHH. 


### -field plaSerialNumber

Append the serial number specified in the <a href="https://msdn.microsoft.com/92bfd307-362e-4d60-9a61-d2096fbb3d19">IDataCollectorSet::SerialNumber</a> property to the subdirectory name in the form NNNNNN. 


### -field plaYearDayOfYear

Append the year and day of the year to the name, in the form yyyyDDD.


### -field plaYearMonth

Append the year and month to the name, in the form yyyyMM.


### -field plaYearMonthDay

Append the year, month, and day to the name, in the form yyyyMMdd.


### -field plaYearMonthDayHour

Append the year, month, day, and hour to the name, in the form yyyyMMddHH.


### -field plaMonthDayHourMinute

Append the month, day, hour, and minute to the name, in the form MMddHHmm.


## -remarks



Patterns apply to files and subdirectories in the same way.

For details on patterns, see the Remarks section of <a href="https://msdn.microsoft.com/94e6bb13-fb99-4968-8a7f-fbda1f6ea42e">FileNameFormatPattern</a>.




## -see-also




<a href="https://msdn.microsoft.com/3a7744a6-feb3-4aea-856d-8496aecc0176">IDataCollector::FileNameFormat</a>



<a href="https://msdn.microsoft.com/f9e6eb88-ac38-4b99-ab64-a408f75f7969">IDataCollectorSet::SubdirectoryFormat</a>
 

 

