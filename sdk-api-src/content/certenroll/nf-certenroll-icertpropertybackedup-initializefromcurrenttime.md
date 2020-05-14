---
UID: NF:certenroll.ICertPropertyBackedUp.InitializeFromCurrentTime
title: ICertPropertyBackedUp::InitializeFromCurrentTime (certenroll.h)
description: Initializes the property from a Boolean value and the current system date and time.helpviewer_keywords: ["ICertPropertyBackedUp interface [Security]","InitializeFromCurrentTime method","ICertPropertyBackedUp.InitializeFromCurrentTime","ICertPropertyBackedUp::InitializeFromCurrentTime","InitializeFromCurrentTime","InitializeFromCurrentTime method [Security]","InitializeFromCurrentTime method [Security]","ICertPropertyBackedUp interface","certenroll/ICertPropertyBackedUp::InitializeFromCurrentTime","security.icertpropertybackedup_initializefromcurrenttime_method"]
old-location: security\icertpropertybackedup_initializefromcurrenttime_method.htm
tech.root: seccertenroll
ms.assetid: 2033c947-661c-4a52-b24f-82fa71ba7868
ms.date: 12/05/2018
ms.keywords: ICertPropertyBackedUp interface [Security],InitializeFromCurrentTime method, ICertPropertyBackedUp.InitializeFromCurrentTime, ICertPropertyBackedUp::InitializeFromCurrentTime, InitializeFromCurrentTime, InitializeFromCurrentTime method [Security], InitializeFromCurrentTime method [Security],ICertPropertyBackedUp interface, certenroll/ICertPropertyBackedUp::InitializeFromCurrentTime, security.icertpropertybackedup_initializefromcurrenttime_method
f1_keywords:
- certenroll/ICertPropertyBackedUp.InitializeFromCurrentTime
dev_langs:
- c++
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
- ICertPropertyBackedUp.InitializeFromCurrentTime
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICertPropertyBackedUp::InitializeFromCurrentTime


## -description


The <b>InitializeFromCurrentTime</b> method initializes the property from a Boolean value and the current system date and time.


## -parameters




### -param BackedUpValue [in]

A <b>VARIANT_BOOL</b> variable that identifies whether the certificate has been backed up.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The object is already initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>HRESULT_FROM_WIN32(ERROR_INVALID_DATA)</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The specified time is not valid.

</td>
</tr>
</table>
 




## -remarks



Internally, the <b>InitializeFromCurrentTime</b> calls the <b>GetSystemTimeAsFileTime</b> function in the Windows SDK. The date is stored as an 8-byte real value, representing a date between January 1, 1900 and December 31, 9999, inclusive. The value 2.0 represents January 1, 1900; 3.0 represents January 2, 1900. Adding 1 to the value increments the date by a day. The fractional part of the value represents the time of day. Therefore, 2.5 represents 12:00 on January 1, 1900; 3.25 represents 06:00 on January 2, 1900.

For dates between 1950 and 2049 inclusive, the date and time is encoded UTC-time in the form YYMMDDHHMMSS. For dates before 1950 or after 2049, encoded generalized time is used. Encoded generalized time is in the form YYYYMMDDHHMMSSMMM, using a four digit year, and is precise to milliseconds.

Call the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icertproperty-setvalueoncertificate">SetValueOnCertificate</a> method to associate the property with a certificate. To retrieve the date, call the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icertpropertybackedup-get_backeduptime">BackedUpTime</a> property. To retrieve the Boolean value that identifies whether a certificate was backed up, call the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icertpropertybackedup-get_backedupvalue">BackedUpValue</a> property.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertpropertybackedup">ICertPropertyBackedUp</a>
 

 

