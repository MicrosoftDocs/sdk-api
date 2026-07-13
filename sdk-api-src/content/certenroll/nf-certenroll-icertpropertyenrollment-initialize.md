---
UID: NF:certenroll.ICertPropertyEnrollment.Initialize
title: ICertPropertyEnrollment::Initialize (certenroll.h)
description: Initializes the property from the certificate request ID, the certification authority (CA) configuration string, and an optional certificate display name.
helpviewer_keywords: ["ICertPropertyEnrollment interface [Security]","Initialize method","ICertPropertyEnrollment.Initialize","ICertPropertyEnrollment::Initialize","Initialize","Initialize method [Security]","Initialize method [Security]","ICertPropertyEnrollment interface","certenroll/ICertPropertyEnrollment::Initialize","security.icertpropertyenrollment_initialize_method"]
old-location: security\icertpropertyenrollment_initialize_method.htm
tech.root: security
ms.assetid: 47e9b11f-3f23-4e2f-817a-4b6311e3d710
ms.date: 12/05/2018
ms.keywords: ICertPropertyEnrollment interface [Security],Initialize method, ICertPropertyEnrollment.Initialize, ICertPropertyEnrollment::Initialize, Initialize, Initialize method [Security], Initialize method [Security],ICertPropertyEnrollment interface, certenroll/ICertPropertyEnrollment::Initialize, security.icertpropertyenrollment_initialize_method
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
 - ICertPropertyEnrollment::Initialize
 - certenroll/ICertPropertyEnrollment::Initialize
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
 - ICertPropertyEnrollment.Initialize
---

# ICertPropertyEnrollment::Initialize


## -description

The <b>Initialize</b> method initializes the property from the certificate request ID, the certification authority (CA) configuration string, and an optional certificate display name.

## -parameters

### -param RequestId [in]

A <b>LONG</b> variable that contains the certificate request ID. A request ID is created by the enrollment process. You can retrieve this value by calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-get_requestid">RequestId</a> property on the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollment">IX509Enrollment</a> interface.

### -param strCADnsName [in]

A <b>BSTR</b> variable that contains the Domain Name System (DNS) name of the CA. This is the first name in the <i>CADnsName\CAName</i> CA configuration string. The configuration string is typically set during the enrollment process. The DNS name can be retrieved by calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-get_caconfigstring">CAConfigString</a> property and separating the  string into its constituent parts.

### -param strCAName [in]

A <b>BSTR</b> variable that contains the subject common name (CN) of the CA. This is the second name in the <i>CADnsName\CAName</i> CA configuration string. The configuration string is typically set during the enrollment process. The CN name can be retrieved by calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-get_caconfigstring">CAConfigString</a> property and separating the  string into its constituent parts.

### -param strFriendlyName [in, optional]

A <b>BSTR</b> variable that contains an optional display name for the certificate. The default value is <b>NULL</b>. This value is typically set during the enrollment process. You can retrieve it by calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-get_certificatefriendlyname">CertificateFriendlyName</a> property.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

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
The object is already initialized.

</td>
</tr>
</table>

## -remarks

The values that you can use to initialize the <a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyenrollment">ICertPropertyEnrollment</a> object are set during the certificate enrollment process when the client calls the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-enroll">Enroll</a> method on the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollment">IX509Enrollment</a> object. That is, to retrieve a request ID, call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-get_requestid">RequestId</a> property on the <b>IX509Enrollment</b> object. To retrieve a certificate display name, call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-get_certificatefriendlyname">CertificateFriendlyName</a> property. To retrieve a distinguished name and common name, call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-get_caconfigstring">CAConfigString</a> property and separate the configuration string into its constituent parts.

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertproperty-setvalueoncertificate">SetValueOnCertificate</a> method to associate the property with a certificate. You can also call the following properties to retrieve the values specified during initialization:<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertyenrollment-get_cadnsname">CADnsName</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertyenrollment-get_caname">CAName</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertyenrollment-get_friendlyname">FriendlyName</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertyenrollment-get_requestid">RequestId</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyenrollment">ICertPropertyEnrollment</a>