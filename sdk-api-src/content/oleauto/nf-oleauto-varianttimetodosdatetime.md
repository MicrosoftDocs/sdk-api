---
UID: NF:oleauto.VariantTimeToDosDateTime
title: VariantTimeToDosDateTime function
author: windows-sdk-content
description: Converts the variant representation of a date and time to MS-DOS date and time values.
old-location: automat\varianttimetodosdatetime.htm
tech.root: automat
ms.assetid: 62307266-2434-4b06-9135-8854f4624c5c
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: VariantTimeToDosDateTime, VariantTimeToDosDateTime function [Automation], _oa96_VariantTimeToDosDateTime, automat.varianttimetodosdatetime, oleauto/VariantTimeToDosDateTime
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - VariantTimeToDosDateTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- VariantTimeToDosDateTime
: 
---

# VariantTimeToDosDateTime function


## -description


Converts the variant representation of a date and time to MS-DOS date and time values.


## -parameters




### -param vtime [in]

The variant time to convert.


### -param pwDosDate [out]

Receives the converted MS-DOS date.


### -param pwDosTime [out]

Receives the converted MS-DOS time


## -returns



The function returns TRUE on success and FALSE otherwise.




## -remarks



A variant time is stored as an 8-byte real value (<b>double</b>), representing a date between January 1, 100 and December 31, 9999, inclusive. The value 2.0 represents January 1, 1900; 3.0 represents January 2, 1900, and so on. Adding 1 to the value increments the date by a day. The fractional part of the value represents the time of day. Therefore, 2.5 represents noon on January 1, 1900; 3.25 represents 6:00 A.M. on January 2, 1900, and so on. Negative numbers represent the dates prior to December 30, 1899.

For a description of the MS-DOS date and time formats, see <a href="61B029CB-8B60-400A-A6BB-A3F6839DC9D2">DosDateTimeToVariantTime</a>.

The <b>VariantTimeToDosDateTime</b> function will accept invalid dates and try to fix them when resolving to a VARIANT time. For example, an invalid date such as 2/29/2001 will resolve to 3/1/2001. Only days are fixed, so invalid month values result in an error being returned. Days are checked to be between 1 and 31. Negative days and days greater than 31 results in an error. A day less than 31 but greater than the maximum day in that month has the day promoted to the appropriate day of the next month. A day equal to zero resolves as the last day of the previous month. For example, an invalid dates such as 2/0/2001 will resolve to 1/31/2001.



