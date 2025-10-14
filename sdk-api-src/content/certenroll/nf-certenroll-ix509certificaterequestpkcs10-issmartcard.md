---
UID: NF:certenroll.IX509CertificateRequestPkcs10.IsSmartCard
title: IX509CertificateRequestPkcs10::IsSmartCard (certenroll.h)
description: Retrieves a Boolean value that indicates whether any of the cryptographic providers associated with the request object is a smart card provider.
helpviewer_keywords: ["IX509CertificateRequestPkcs10 interface [Security]","IsSmartCard method","IX509CertificateRequestPkcs10.IsSmartCard","IX509CertificateRequestPkcs10::IsSmartCard","IsSmartCard","IsSmartCard method [Security]","IsSmartCard method [Security]","IX509CertificateRequestPkcs10 interface","certenroll/IX509CertificateRequestPkcs10::IsSmartCard","security.ix509certificaterequestpkcs10_issmartcard_method"]
old-location: security\ix509certificaterequestpkcs10_issmartcard_method.htm
tech.root: security
ms.assetid: 663ca7dd-f108-46bf-9564-cd2d7ec2bb1f
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestPkcs10 interface [Security],IsSmartCard method, IX509CertificateRequestPkcs10.IsSmartCard, IX509CertificateRequestPkcs10::IsSmartCard, IsSmartCard, IsSmartCard method [Security], IsSmartCard method [Security],IX509CertificateRequestPkcs10 interface, certenroll/IX509CertificateRequestPkcs10::IsSmartCard, security.ix509certificaterequestpkcs10_issmartcard_method
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
 - IX509CertificateRequestPkcs10::IsSmartCard
 - certenroll/IX509CertificateRequestPkcs10::IsSmartCard
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
 - IX509CertificateRequestPkcs10.IsSmartCard
---

# IX509CertificateRequestPkcs10::IsSmartCard


## -description

The <b>IsSmartCard</b> method retrieves a Boolean value that indicates whether any of the cryptographic providers associated with the request object is a smart card provider.

## -parameters

### -param pValue [out]

Pointer to a <b>VARIANT_BOOL</b> variable that indicates whether any of the enumerated and selected providers is  a smart card provider.

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
<dt><b>CERTSRV_E_PROPERTY_EMPTY</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The private key cannot be found, or the <a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a> object associated with the private key cannot be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_BLANK</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The object is not initialized.

</td>
</tr>
</table>

## -remarks

The <b>IsSmartCard</b> method first checks the provider associated with the private key. If that provider is not for a smart card, the method iterates through the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_cspstatuses">CspStatuses</a> collection until it finds a selected provider that is. If no selected smart card providers are found, the method returns <b>False</b>. You must initialize the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a> object before calling this method. For more information, see any of the following methods:

<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializedecode">InitializeDecode</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromcertificate">InitializeFromCertificate</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromprivatekey">InitializeFromPrivateKey</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefrompublickey">InitializeFromPublicKey</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromtemplatename">InitializeFromTemplateName</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>