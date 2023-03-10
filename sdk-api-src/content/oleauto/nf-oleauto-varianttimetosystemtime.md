---
UID: NF:oleauto.VariantTimeToSystemTime
title: VariantTimeToSystemTime function (oleauto.h)
description: Converts the variant representation of time to system time values.
helpviewer_keywords: ["VariantTimeToSystemTime","VariantTimeToSystemTime function [Automation]","_oa96_VariantTimeToSystemTime","automat.varianttimetosystemtime","oleauto/VariantTimeToSystemTime"]
old-location: automat\varianttimetosystemtime.htm
tech.root: automat
ms.assetid: 954eb6f3-f9f0-4586-9dd7-1632ebc6ef58
ms.date: 12/05/2018
ms.keywords: VariantTimeToSystemTime, VariantTimeToSystemTime function [Automation], _oa96_VariantTimeToSystemTime, automat.varianttimetosystemtime, oleauto/VariantTimeToSystemTime
req.header: oleauto.h
req.include-header: 
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
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VariantTimeToSystemTime
 - oleauto/VariantTimeToSystemTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - VariantTimeToSystemTime
---

# VariantTimeToSystemTime function


## -description

Converts the variant representation of time to system time values.

## -parameters

### -param vtime [in]

The variant time to convert.

### -param lpSystemTime [out]

Receives the system time.

## -returns

The function returns TRUE on success and FALSE otherwise.

## -remarks

A variant time is stored as an 8-byte real value (<b>double</b>), representing a date between January 1, 100 and December 31, 9999, inclusive. The value 2.0 represents January 1, 1900; 3.0 represents January 2, 1900, and so on. Adding 1 to the value increments the date by a day. The fractional part of the value represents the time of day. Therefore, 2.5 represents noon on January 1, 1900; 3.25 represents 6:00 A.M. on January 2, 1900, and so on. Negative numbers represent the dates prior to December 30, 1899.

Using the SYSTEMTIME structure is useful because:  

<ul>
<li>
It spans all time/date periods. MS-DOS date/time is limited to representing only those dates between 1/1/1980 and 12/31/2107. 

</li>
<li>
The date/time elements are all easily accessible without needing to do any bit decoding.

</li>
<li>
The National Language Support data and time formatting functions <b>GetDateFormat</b> and <b>GetTimeFormat</b> take a SYSTEMTIME value as input.

</li>
<li>
It is the default Win32 time and date data format supported by Windows NT and Windows 95.

</li>
</ul>
The <b>VariantTimeToSystemTime</b> function will accept invalid dates and try to fix them when resolving to a VARIANT time. For example, an invalid date such as 2/29/2001 will resolve to 3/1/2001. Only days are fixed, so invalid month values result in an error being returned. Days are checked to be between 1 and 31. Negative days and days greater than 31 results in an error. A day less than 31 but greater than the maximum day in that month has the day promoted to the appropriate day of the next month. A day equal to zero resolves as the last day of the previous month. For example, an invalid dates such as 2/0/2001 will resolve to 1/31/2001.

