---
UID: NF:certenroll.IX509CertificateRequestPkcs7.InitializeFromTemplateName
title: IX509CertificateRequestPkcs7::InitializeFromTemplateName
author: windows-sdk-content
description: Initializes the certificate request by using a template.
old-location: security\ix509certificaterequestpkcs7_initializefromtemplatename_method.htm
old-project: SecCertEnroll
ms.assetid: d6c15fcb-1883-4d87-af29-721102676535
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IX509CertificateRequestPkcs7 interface [Security],InitializeFromTemplateName method, IX509CertificateRequestPkcs7.InitializeFromTemplateName, IX509CertificateRequestPkcs7::InitializeFromTemplateName, InitializeFromTemplateName, InitializeFromTemplateName method [Security], InitializeFromTemplateName method [Security],IX509CertificateRequestPkcs7 interface, certenroll/IX509CertificateRequestPkcs7::InitializeFromTemplateName, security.ix509certificaterequestpkcs7_initializefromtemplatename_method
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	IX509CertificateRequestPkcs7.InitializeFromTemplateName
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequestPkcs7::InitializeFromTemplateName


## -description


The <b>InitializeFromTemplateName</b> method initializes the certificate request by using a template.


## -parameters




### -param Context [in]

An <a href="https://msdn.microsoft.com/2db0e129-a566-47ba-ab57-53c7db09e8e3">X509CertificateEnrollmentContext</a> enumeration value that specifies whether the requested certificate is intended for an end user, a computer, or an administrator acting on behalf of the computer.


### -param strTemplateName [in]

A  <b>BSTR</b> variable that contains the Common Name (CN) of the template as it appears in Active Directory or the dotted decimal <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a>.


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
<dt><b><b>ERROR_ALREADY_INITIALIZED</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The certificate request object has already been initialized.

</td>
</tr>
</table>
 




## -remarks



The <b>InitializeFromTemplateName</b> method creates a PKCS #7 request object and sets the following properties to the values that existed before this method was called:

<ul>
<li>
<a href="https://msdn.microsoft.com/7be532ab-0ab0-4c22-b274-c925fd5827d5">CspInformations</a>
</li>
<li>
<a href="https://msdn.microsoft.com/86e82a6c-7689-4bf3-8f64-e512040abd6a">ParentWindow</a>
</li>
<li>
<a href="https://msdn.microsoft.com/339c8d47-4406-4f2e-b927-b2dd5f58d1ec">Silent</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0eedb520-06c3-4106-8593-1c5fb0829d5e">UIContextMessage</a>
</li>
</ul>
The method creates the following collections:<ul>
<li>An <a href="https://msdn.microsoft.com/beedb57c-1c89-4d16-8514-046e3071fd1e">ICryptAttributes</a> collection.</li>
<li>An <a href="https://msdn.microsoft.com/d6bdbcff-1d6b-4813-8269-b75061a42de8">IX509Extensions</a> collection.</li>
<li>An <a href="https://msdn.microsoft.com/f376a33e-005b-4810-9a26-b642236ff7af">IObjectIds</a> collection populated with the default XCN_OID_KEY_USAGE and XCN_OID_BASIC_CONSTRAINTS2 object identifiers.</li>
<li>An empty <a href="https://msdn.microsoft.com/f376a33e-005b-4810-9a26-b642236ff7af">IObjectIds</a> collection for attribute and extension OIDs to be suppressed from the new request.</li>
</ul>


The method then examines the template and performs the following actions:<ul>
<li>Adds the extensions specified by the template to the <a href="https://msdn.microsoft.com/d6bdbcff-1d6b-4813-8269-b75061a42de8">IX509Extensions</a> collection.</li>
<li>Removes the default critical extensions (XCN_OID_KEY_USAGE and XCN_OID_BASIC_CONSTRAINTS2) from the collection if the template indicates that they are not critical. The OIDs marked critical by the template are added.</li>
<li>Sets the <a href="https://msdn.microsoft.com/5aa027d7-3c31-4b70-92a5-d15d2c410366">SmimeCapabilities</a> property if the template supports symmetric algorithms.</li>
<li>Sets the <a href="https://msdn.microsoft.com/57a87aab-1e53-4b0b-a7b9-2fe89083819b">AlternateSignatureAlgorithm</a> property if the template requires a discrete signature algorithm OID.</li>
<li>Creates an <a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a> object.</li>
<li>Creates a hash algorithm OID if the algorithm is specified in the template and sets it on the <a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a> object.</li>
<li>Creates an asymmetric encryption algorithm OID if the algorithm is specified in the template and sets it on the <a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a> object.</li>
<li>Sets the following <a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a> properties from the template settings:<ul>
<li>
<a href="https://msdn.microsoft.com/163e0fb5-e5b1-48db-a90f-66984530f92f">KeySpec</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e983c95b-6b3a-4e27-8a23-ef9051b11a16">KeyUsage</a>
</li>
<li>
<a href="https://msdn.microsoft.com/de25aa05-bd65-49a6-9cd1-e18522c9e190">Length</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e3f04252-fe49-48fb-9e77-8a05031abf5f">ExportPolicy</a>
</li>
<li>
<a href="https://msdn.microsoft.com/39d8b9ac-ebbd-4bd8-8d5e-a4b28595b030">KeyProtection</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5fa1e5d8-b745-494c-a727-426084fce2a1">SecurityDescriptor</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4f61a513-620c-48c4-b9dd-032b13a9f654">Silent</a>
</li>
<li>
<a href="https://msdn.microsoft.com/bdc3278e-3b5a-4ad0-9e9b-9639a2db4040">MachineContext</a>
</li>
<li>
<a href="https://msdn.microsoft.com/40d2eae1-733a-4e5b-bb15-71301d73f438">Algorithm</a>
</li>
</ul>
</li>
</ul>


If the <a href="https://msdn.microsoft.com/7be532ab-0ab0-4c22-b274-c925fd5827d5">CSPInformations</a> property is <b>NULL</b>, the method creates an <a href="https://msdn.microsoft.com/8141023c-c162-46d6-9c37-e227ce1c8761">ICspInformations</a> collection from the providers installed on the computer.

Finally, the method sets the initialized PKCS #10 request as the inner request object.




## -see-also




<a href="https://msdn.microsoft.com/ae869557-6523-4387-835e-c9631898d864">IX509CertificateRequestPkcs7</a>
 

 

