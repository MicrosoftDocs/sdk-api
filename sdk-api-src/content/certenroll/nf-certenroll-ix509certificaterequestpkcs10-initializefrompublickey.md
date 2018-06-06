---
UID: NF:certenroll.IX509CertificateRequestPkcs10.InitializeFromPublicKey
title: IX509CertificateRequestPkcs10::InitializeFromPublicKey
author: windows-sdk-content
description: Initializes a null-signed certificate request by using an IX509PublicKey object and, optionally, a template.
old-location: security\ix509certificaterequestpkcs10_initializefrompublickey_method.htm
old-project: SecCertEnroll
ms.assetid: 7b7e00dc-649b-4bcb-a9b6-5745b33ea48b
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IX509CertificateRequestPkcs10 interface [Security],InitializeFromPublicKey method, IX509CertificateRequestPkcs10.InitializeFromPublicKey, IX509CertificateRequestPkcs10::InitializeFromPublicKey, InitializeFromPublicKey, InitializeFromPublicKey method [Security], InitializeFromPublicKey method [Security],IX509CertificateRequestPkcs10 interface, certenroll/IX509CertificateRequestPkcs10::InitializeFromPublicKey, security.ix509certificaterequestpkcs10_initializefrompublickey_method
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509CertificateRequestPkcs10.InitializeFromPublicKey
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequestPkcs10::InitializeFromPublicKey


## -description


The <b>InitializeFromPublicKey</b> method initializes a null-signed certificate request by using an <a href="https://msdn.microsoft.com/cd6f28a3-9998-40d7-a3e8-dab0cf3991a8">IX509PublicKey</a> object and, optionally, a template.


## -parameters




### -param Context [in]

An <a href="https://msdn.microsoft.com/2db0e129-a566-47ba-ab57-53c7db09e8e3">X509CertificateEnrollmentContext</a> enumeration value that specifies whether the requested certificate is intended for an end user, a computer, or an administrator acting on behalf of the computer.


### -param pPublicKey [in]

Pointer to an <a href="https://msdn.microsoft.com/cd6f28a3-9998-40d7-a3e8-dab0cf3991a8">IX509PublicKey</a> interface that represents the public key.


### -param strTemplateName [in, optional]

A  <b>BSTR</b> variable that contains the Common Name (CN) of the template as it appears in Active Directory or the dotted decimal <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a>. This is an optional parameter.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

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
The certificate request object has already been initialized.

</td>
</tr>
</table>
 




## -remarks



If you specify a template, the <b>InitializeFromPublicKey</b> method performs the following actions:<ul>
<li>Adds the extensions specified in the optional template, if any, to the <a href="https://msdn.microsoft.com/d6bdbcff-1d6b-4813-8269-b75061a42de8">IX509Extensions</a> collection.</li>
<li>Creates a <a href="https://msdn.microsoft.com/7ecde7cb-1a73-4fee-a949-c4bb36e61547">CriticalExtensions</a> collection and populates it with the default XCN_OID_KEY_USAGE and XCN_OID_BASIC_CONSTRAINTS2 object identifiers. If a template is specified and indicates that these OIDs are not critical, they are removed from the collection. The OIDs marked critical by the template, if any,  are added.</li>
<li>Sets the <a href="https://msdn.microsoft.com/5aa027d7-3c31-4b70-92a5-d15d2c410366">SmimeCapabilities</a> property if the template supports symmetric algorithms.</li>
<li>Sets the <a href="https://msdn.microsoft.com/57a87aab-1e53-4b0b-a7b9-2fe89083819b">AlternateSignatureAlgorithm</a> property if the template requires a discrete signature algorithm OID.</li>
<li>Creates an <a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a> object.</li>
<li>Creates a hash algorithm OID if the algorithm is specified in the template and sets it on the <a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a> object.</li>
<li>Creates an asymmetric encryption algorithm OID if the algorithm is specified in the template and sets it on the <a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a> object.</li>
</ul>


Whether you specify a template or not, if the <a href="https://msdn.microsoft.com/7be532ab-0ab0-4c22-b274-c925fd5827d5">CSPInformations</a> property is not specified, the method creates an <a href="https://msdn.microsoft.com/8141023c-c162-46d6-9c37-e227ce1c8761">ICspInformations</a> collection from the providers installed on the computer.

The method does not create a private key. The use of this method implies that the request is null-signed. Therefore, the method sets the <a href="https://msdn.microsoft.com/a693343e-7c9a-4967-b46c-53936497662a">NullSigned</a> property on the  <a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a> object.




## -see-also




<a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a>
 

 

