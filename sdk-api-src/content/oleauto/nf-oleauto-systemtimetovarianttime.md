---
UID: NF:oleauto.SystemTimeToVariantTime
title: SystemTimeToVariantTime function (oleauto.h)
description: Converts a system time to a variant representation.
helpviewer_keywords: ["SystemTimeToVariantTime","SystemTimeToVariantTime function [Automation]","_oa96_SystemTimeToVariantTime","automat.systemtimetovarianttime","oleauto/SystemTimeToVariantTime"]
old-location: automat\systemtimetovarianttime.htm
tech.root: automat
ms.assetid: d9d69521-9b33-4fc5-8a1c-929f216db450
ms.date: 12/05/2018
ms.keywords: SystemTimeToVariantTime, SystemTimeToVariantTime function [Automation], _oa96_SystemTimeToVariantTime, automat.systemtimetovarianttime, oleauto/SystemTimeToVariantTime
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
 - SystemTimeToVariantTime
 - oleauto/SystemTimeToVariantTime
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
 - SystemTimeToVariantTime
---

# SystemTimeToVariantTime function


## -description

Converts a system time to a variant representation.

## -parameters

### -param lpSystemTime [in]

The system time.

### -param pvtime [out]

The variant time.

## -returns

The function returns TRUE on success and FALSE otherwise.

## -remarks

A variant time is stored as an 8-byte real value (<b>double</b>), representing a date between January 1, 1900 and December 31, 9999, inclusive. The value 2.0 represents January 1, 1900; 3.0 represents January 2, 1900, and so on. Adding 1 to the value increments the date by a day. The fractional part of the value represents the time of day. Therefore, 2.5 represents noon on January 1, 1900; 3.25 represents 6:00 A.M. on January 2, 1900, and so on. Negative numbers represent dates prior to December 30, 1899.

The variant time resolves to one second. Any milliseconds in the input date are ignored. 

> [!NOTE]
> When working with variant time, be mindful of the additional day added in leap years, which might produce unexpected results if unhandled. For more information, see [leap year readiness](https://techcommunity.microsoft.com/t5/azure-developer-community-blog/it-s-2020-is-your-code-ready-for-leap-day/ba-p/1157279).

The <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure is useful for the following reasons:  

<ul>
<li>
It spans all time/date periods. MS-DOS date/time is limited to representing only those dates between 1/1/1980 and 12/31/2107. 

</li>
<li>
The date/time elements are all easily accessible without needing to do any bit decoding.

</li>
<li>
The National Data Support data and time formatting functions <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata">GetDateFormat</a> and <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata">GetTimeFormat</a> take an <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">LPSYSTEMTIME</a> value as input.

</li>
<li>
It is the default time/date data format supported by Windows.

</li>
</ul>
The <b>SystemTimeToVariantTime</b> function will accept invalid dates and try to fix them when resolving to a VARIANT time. For example, an invalid date such as 2/29/2001 will resolve to 3/1/2001. Only days are fixed, so invalid month values result in an error being returned. Days are checked to be between 1 and 31. Negative days and days greater than 31 results in an error. A day less than 31 but greater than the maximum day in that month has the day promoted to the appropriate day of the next month. A day equal to zero resolves as the last day of the previous month. For example, an invalid dates such as 2/0/2001 will resolve to 1/31/2001.
