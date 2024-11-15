---
UID: NF:winbio.WinBioGetEnrolledFactors
title: WinBioGetEnrolledFactors function (winbio.h)
description: Gets information about the biometric enrollments that the specified user has on the computer.
helpviewer_keywords: ["WinBioGetEnrolledFactors","WinBioGetEnrolledFactors function [Windows Biometric Framework API]","secbiomet.winbiogetenrolledfactors","winbio/WinBioGetEnrolledFactors"]
old-location: secbiomet\winbiogetenrolledfactors.htm
tech.root: SecBioMet
ms.assetid: 25DCB7FC-6971-4EFD-A686-E994F4345D2B
ms.date: 12/05/2018
ms.keywords: WinBioGetEnrolledFactors, WinBioGetEnrolledFactors function [Windows Biometric Framework API], secbiomet.winbiogetenrolledfactors, winbio/WinBioGetEnrolledFactors
req.header: winbio.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winbio.lib
req.dll: Winbio.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WinBioGetEnrolledFactors
 - winbio/WinBioGetEnrolledFactors
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - winbio.dll
 - Ext-MS-Win-Biometrics-WinBio-Core-L1-1-0.dll
 - Ext-MS-Win-BioMetrics-WinBio-Core-L1-1-1.dll
api_name:
 - WinBioGetEnrolledFactors
---

# WinBioGetEnrolledFactors function


## -description

Gets information about the biometric enrollments that the specified user has on the computer. Biometric enrollments include enrollments for facial recognition, fingerprint scanning, iris scanning, and so on.

## -parameters

### -param AccountOwner [in]

A <a href="/windows/desktop/SecBioMet/winbio-identity">WINBIO_IDENTITY</a> structure for the user whose biometric enrollments you want to get. For example:


``` syntax
WINBIO_IDENTITY identity = {};
identity.Type = WINBIO_ID_TYPE_SID;

// Move an account SID into identity.Value.AccountSid.Data.
// For example, CopySid(...)
```

To see the enrollments for every user on the computer, specify the  <b>WINBIO_ID_TYPE_WILDCARD</b> identity type for the <a href="/windows/desktop/SecBioMet/winbio-identity">WINBIO_IDENTITY</a> structure that you specify for the <i>AccountOwner</i> parameter. For example:


``` syntax
WINBIO_IDENTITY identity = {};
identity.Type = WINBIO_ID_TYPE_WILDCARD;

```


### -param EnrolledFactors [out]

A set of <a href="/windows/desktop/SecBioMet/winbio-biometric-type-constants">WINBIO_BIOMETRIC_TYPE</a> flags that indicate the biometric enrollments that the specified user has on the computer. A value of 0 indicates that the user has no biometric enrollments.

These enrollments represent system pool enrollments only, such as enrollments that you can use to authenticate a user for sign-in, unlock, and so on.          This value does not include private pool enrollments.

If you specify the wildcard identity type for the  <a href="/windows/desktop/SecBioMet/winbio-identity">WINBIO_IDENTITY</a> structure that you use for the <i>AccountOwner</i> parameter, this set of flags represents the combined set of enrollments for all users with accounts on the computer.

## -returns

If the function succeeds, it returns <b>S_OK</b>. If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>AccountOwner</i> and <i>EnrolledFactors</i> parameters cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <b>Type</b> member of the <a href="/windows/desktop/SecBioMet/winbio-identity">WINBIO_IDENTITY</a> structure that the  <i>AccountOnwer</i> parameter specified was not <b>WINBIO_ID_TYPE_SID</b> or <b>WINBIO_ID_TYPE_WILDCARD</b>, or the <b>AccountSid</b> member of the <b>WINBIO_IDENTITY</b> structure was not valid.

</td>
</tr>
</table>

## -remarks

<b>WinBioGetEnrolledFactors</b> does not require a biometric session handle and does not activate the biometric service. Consequently, <b>WinBioGetEnrolledFactors</b> runs quickly and is useful when your code needs to make quick decisions about how to proceed when time is critical for the set of operations you need to perform.

<b>WinBioGetEnrolledFactors</b> provides credential providers with a way to tailor their UI appropriately. For example, the login screen calls  <b>WinBioGetEnrolledFactors</b> to determine whether to display the option to login with a fingerprint.


#### Examples


``` syntax
WINBIO_BIOMETRIC_TYPE enrolledFactors = WINBIO_NO_TYPE_AVAILABLE;

WINBIO_IDENTITY identity = {};
identity.Type = WINBIO_ID_TYPE_SID;

// Move an account SID into identity.Value.AccountSid.Data.
// e.g., CopySid(...)

HRESULT hr = WinBioGetEnrolledFactors(&identity, &enrolledFactors);

```


## -see-also

<a href="/windows/desktop/SecBioMet/winbio-biometric-type-constants">WINBIO_BIOMETRIC_TYPE</a>



<a href="/windows/desktop/SecBioMet/winbio-identity">WINBIO_IDENTITY</a>
