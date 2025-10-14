---
UID: NF:certenroll.IX509Enrollment.Initialize
title: IX509Enrollment::Initialize (certenroll.h)
description: Initializes the enrollment object and creates a default PKCS
helpviewer_keywords: ["IX509Enrollment interface [Security]","Initialize method","IX509Enrollment.Initialize","IX509Enrollment::Initialize","Initialize","Initialize method [Security]","Initialize method [Security]","IX509Enrollment interface","certenroll/IX509Enrollment::Initialize","security.ix509enrollment_initialize_method"]
old-location: security\ix509enrollment_initialize_method.htm
tech.root: security
ms.assetid: 3bf4ce4a-6556-403c-8334-a6bf01f074a3
ms.date: 12/05/2018
ms.keywords: IX509Enrollment interface [Security],Initialize method, IX509Enrollment.Initialize, IX509Enrollment::Initialize, Initialize, Initialize method [Security], Initialize method [Security],IX509Enrollment interface, certenroll/IX509Enrollment::Initialize, security.ix509enrollment_initialize_method
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
 - IX509Enrollment::Initialize
 - certenroll/IX509Enrollment::Initialize
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
 - IX509Enrollment.Initialize
---

# IX509Enrollment::Initialize


## -description

The <b>Initialize</b> method initializes the enrollment object and creates a default PKCS #10 request. This method is web enabled.

## -parameters

### -param Context [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-x509certificateenrollmentcontext">X509CertificateEnrollmentContext</a> enumeration value that specifies whether the requested enrollment is for a user, a computer, or an administrator acting on behalf of a computer.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The enrollment object has already been initialized.

</td>
</tr>
</table>

## -remarks

The <b>Initialize</b> method creates a new key pair and initializes empty collections for the attributes, extensions and critical extensions associated with the request.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollment">IX509Enrollment</a>