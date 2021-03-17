---
UID: NF:certenroll.ICertPropertyBackedUp.get_BackedUpTime
title: ICertPropertyBackedUp::get_BackedUpTime (certenroll.h)
description: Retrieves the date and time at which the certificate was backed up.
helpviewer_keywords: ["BackedUpTime property [Security]","BackedUpTime property [Security]","ICertPropertyBackedUp interface","ICertPropertyBackedUp interface [Security]","BackedUpTime property","ICertPropertyBackedUp.BackedUpTime","ICertPropertyBackedUp.get_BackedUpTime","ICertPropertyBackedUp::BackedUpTime","ICertPropertyBackedUp::get_BackedUpTime","certenroll/ICertPropertyBackedUp::BackedUpTime","certenroll/ICertPropertyBackedUp::get_BackedUpTime","get_BackedUpTime","security.icertpropertybackedup_backeduptime_property"]
old-location: security\icertpropertybackedup_backeduptime_property.htm
tech.root: security
ms.assetid: 5515fbd5-a711-421d-b80d-3e77c83f7549
ms.date: 12/05/2018
ms.keywords: BackedUpTime property [Security], BackedUpTime property [Security],ICertPropertyBackedUp interface, ICertPropertyBackedUp interface [Security],BackedUpTime property, ICertPropertyBackedUp.BackedUpTime, ICertPropertyBackedUp.get_BackedUpTime, ICertPropertyBackedUp::BackedUpTime, ICertPropertyBackedUp::get_BackedUpTime, certenroll/ICertPropertyBackedUp::BackedUpTime, certenroll/ICertPropertyBackedUp::get_BackedUpTime, get_BackedUpTime, security.icertpropertybackedup_backeduptime_property
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertPropertyBackedUp::get_BackedUpTime
 - certenroll/ICertPropertyBackedUp::get_BackedUpTime
dev_langs:
 - c++
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
---

# ICertPropertyBackedUp::get_BackedUpTime


## -description

The <b>BackedUpTime</b> property retrieves the date and time at which the certificate was backed up.

This property is read-only.

## -parameters

## -remarks

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertybackedup-initialize">Initialize</a> method or the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertybackedup-initializefromcurrenttime">InitializeFromCurrentTime</a> method to set the <b>BackedUpTime</b> value.

The date is stored as an 8-byte real value, representing a date between January 1, 1900 and December 31, 9999, inclusive. The value 2.0 represents January 1, 1900; 3.0 represents January 2, 1900. Adding 1 to the value increments the date by a day. The fractional part of the value represents the time of day. Therefore, 2.5 represents 12:00 on January 1, 1900; 3.25 represents 06:00 on January 2, 1900.

For dates between 1950 and 2049 inclusive, the date and time is encoded UTC-time in the form YYMMDDHHMMSS. For dates before 1950 or after 2049, encoded generalized time is used. Encoded generalized time is in the form YYYYMMDDHHMMSSMMM, using a four digit year, and is precise to milliseconds.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertybackedup">ICertPropertyBackedUp</a>