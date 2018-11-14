---
UID: NF:certenroll.ICertPropertyBackedUp.get_BackedUpTime
title: ICertPropertyBackedUp::get_BackedUpTime
author: windows-sdk-content
description: Retrieves the date and time at which the certificate was backed up.
old-location: security\icertpropertybackedup_backeduptime_property.htm
tech.root: SecCertEnroll
ms.assetid: 5515fbd5-a711-421d-b80d-3e77c83f7549
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: BackedUpTime property [Security], BackedUpTime property [Security],ICertPropertyBackedUp interface, ICertPropertyBackedUp interface [Security],BackedUpTime property, ICertPropertyBackedUp.BackedUpTime, ICertPropertyBackedUp.get_BackedUpTime, ICertPropertyBackedUp::BackedUpTime, ICertPropertyBackedUp::get_BackedUpTime, certenroll/ICertPropertyBackedUp::BackedUpTime, certenroll/ICertPropertyBackedUp::get_BackedUpTime, get_BackedUpTime, security.icertpropertybackedup_backeduptime_property
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certenroll.h
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
req.dll: CertEnroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - ICertPropertyBackedUp.BackedUpTime
 - ICertPropertyBackedUp.get_BackedUpTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- certenroll.h
: 
- ICertPropertyBackedUp.get_BackedUpTime
: 
---

# ICertPropertyBackedUp::get_BackedUpTime


## -description


The <b>BackedUpTime</b> property retrieves the date and time at which the certificate was backed up.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/en-us/library/Aa375630(v=VS.85).aspx">Initialize</a> method or the <a href="https://msdn.microsoft.com/en-us/library/Aa375364(v=VS.85).aspx">InitializeFromCurrentTime</a> method to set the <b>BackedUpTime</b> value.

The date is stored as an 8-byte real value, representing a date between January 1, 1900 and December 31, 9999, inclusive. The value 2.0 represents January 1, 1900; 3.0 represents January 2, 1900. Adding 1 to the value increments the date by a day. The fractional part of the value represents the time of day. Therefore, 2.5 represents 12:00 on January 1, 1900; 3.25 represents 06:00 on January 2, 1900.

For dates between 1950 and 2049 inclusive, the date and time is encoded UTC-time in the form YYMMDDHHMMSS. For dates before 1950 or after 2049, encoded generalized time is used. Encoded generalized time is in the form YYYYMMDDHHMMSSMMM, using a four digit year, and is precise to milliseconds.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa375239(v=VS.85).aspx">ICertProperty</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375353(v=VS.85).aspx">ICertPropertyBackedUp</a>
 

 

