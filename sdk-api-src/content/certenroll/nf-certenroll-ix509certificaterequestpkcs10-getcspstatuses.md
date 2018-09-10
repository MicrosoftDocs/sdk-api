---
UID: NF:certenroll.IX509CertificateRequestPkcs10.GetCspStatuses
title: IX509CertificateRequestPkcs10::GetCspStatuses
author: windows-sdk-content
description: Retrieves an ICspStatuses collection that contains all provider/algorithm pairs consistent with the intended use of the private key as specified by the caller.
old-location: security\ix509certificaterequestpkcs10_getcspstatuses_method.htm
tech.root: SecCertEnroll
ms.assetid: 50dc8cc5-21ee-4347-a12a-0d6e62901fbb
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetCspStatuses, GetCspStatuses method [Security], GetCspStatuses method [Security],IX509CertificateRequestPkcs10 interface, IX509CertificateRequestPkcs10 interface [Security],GetCspStatuses method, IX509CertificateRequestPkcs10.GetCspStatuses, IX509CertificateRequestPkcs10::GetCspStatuses, XCN_AT_KEYEXCHANGE, XCN_AT_NONE, XCN_AT_SIGNATURE, certenroll/IX509CertificateRequestPkcs10::GetCspStatuses, security.ix509certificaterequestpkcs10_getcspstatuses_method
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
 - IX509CertificateRequestPkcs10.GetCspStatuses
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequestPkcs10::GetCspStatuses


## -description


The <b>GetCspStatuses</b> method retrieves an <a href="https://msdn.microsoft.com/73d0f3a7-7afd-42c9-88db-911531c50137">ICspStatuses</a> collection that contains all provider/algorithm pairs consistent with the intended use of the private key as specified by the caller.


## -parameters




### -param KeySpec [in]

An <a href="https://msdn.microsoft.com/d677d46c-3b36-4081-a6db-123ac1cef84b">X509KeySpec</a> enumeration value that specifies the intended use of the key. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="XCN_AT_NONE"></a><a id="xcn_at_none"></a><dl>
<dt><b>XCN_AT_NONE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Only Cryptography API: Next Generation (CNG) providers are selected.

</td>
</tr>
<tr>
<td width="40%"><a id="XCN_AT_KEYEXCHANGE"></a><a id="xcn_at_keyexchange"></a><dl>
<dt><b>XCN_AT_KEYEXCHANGE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Only CryptoAPI <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service providers</a> (CSPs) with encryption algorithms (including key exchange) are selected.

</td>
</tr>
<tr>
<td width="40%"><a id="XCN_AT_SIGNATURE"></a><a id="xcn_at_signature"></a><dl>
<dt><b>XCN_AT_SIGNATURE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Only CryptoAPI CSPs with signature algorithms are selected.

</td>
</tr>
</table>
 


### -param ppCspStatuses [out]

Address of a variable that receives a pointer to an  <a href="https://msdn.microsoft.com/73d0f3a7-7afd-42c9-88db-911531c50137">ICspStatuses</a> interface that represents the collection.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CERTSRV_E_PROPERTY_EMPTY</b></dt>
</dl>
</td>
<td width="60%">
The private key cannot be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_BLANK</b></dt>
</dl>
</td>
<td width="60%">
The object is not initialized.

</td>
</tr>
</table>
 




## -remarks



This method retrieves a collection of <a href="https://msdn.microsoft.com/30cc43c8-6ef3-49ad-8cff-9a5b7389ff68">ICspStatus</a> objects. Each object represents a single provider/algorithm pair. If you specify a template when initializing the <a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a> request object, template attributes  such as the  <b>pKIDefaultCSPs</b> and <b>pKIDefaultKeySpec</b> affect which pairs are initially enabled. You can call the following properties on each <b>ICspStatus</b> object to retrieve information about a pair:<ul>
<li>The <a href="https://msdn.microsoft.com/9e9202ad-086e-493b-8830-0a0f8980cec5">CspInformation</a> property retrieves provider information.</li>
<li>The <a href="https://msdn.microsoft.com/fc86ff4a-98f4-4e14-8d24-132926c9b41d">CspAlgorithm</a> property retrieves algorithm information.</li>
<li>The <a href="https://msdn.microsoft.com/56798477-ec12-47b6-a226-d20258677033">EnrollmentStatus</a> property retrieves an <a href="https://msdn.microsoft.com/fa5e3a10-7f00-46b6-b740-b72d78745bf7">IX509EnrollmentStatus</a> object. Call the <a href="https://msdn.microsoft.com/9050f394-ccad-4a6e-90bc-53af3a874f91">Selected</a> property on the status object to determine whether the provider/algorithm pair is enabled for this request.</li>
<li>The <a href="https://msdn.microsoft.com/e392e28f-084e-43a7-8a5e-14bea0ed8d58">Ordinal</a> property retrieves the position in the provider/algorithm pair collection.</li>
</ul>


The collection retrieved by this method is saved internally on the request object. Up to three collections, one for each <i>KeySpec</i> value, can be created and saved. This is done to preserve the selection state of the provider/algorithm pairs so that relevant property pages can be displayed accurately and quickly multiple times and so that the <a href="https://msdn.microsoft.com/098788f4-539f-420b-a4e1-65625dd56ca1">Encode</a> method can identify which providers and algorithms are selected if a private key must be created. If the selection state of a provider/algorithm pair is modified, the changes are saved to the appropriate collection. Changes made to the members of one collection do not affect the members of any other collection. The collections exist as long as the PKCS #10 object continues to exist.

Assume, for example, that this method is called with the <i>KeySpec</i> parameter set to XCN_AT_SIGNATURE and that a template is used to initialize the request. The following statements will be true:<ul>
<li>A collection of <a href="https://msdn.microsoft.com/30cc43c8-6ef3-49ad-8cff-9a5b7389ff68">ICspStatus</a> objects is created and saved on the <a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a> object. The collection contains all valid provider/algorithm pairs installed on the computer.</li>
<li>Because the <i>KeySpec</i> parameter is not set to XCN_AT_NONE, the <a href="https://msdn.microsoft.com/9050f394-ccad-4a6e-90bc-53af3a874f91">Selected</a> property is set to SelectedNo for each Cryptography API: Next Generation (CNG) provider/algorithm pair in the collection.</li>
<li>Because the <i>KeySpec</i> parameter is not set to XCN_AT_KEYEXCHANGE, the <a href="https://msdn.microsoft.com/9050f394-ccad-4a6e-90bc-53af3a874f91">Selected</a> property is set to SelectedNo for each CryptoAPI CSP/algorithm pair in the collection where the algorithm can be used to encrypt data or archive a key.</li>
<li>For each provider referenced by the template or private key but not supported on the computer, a placeholder <a href="https://msdn.microsoft.com/30cc43c8-6ef3-49ad-8cff-9a5b7389ff68">ICspStatus</a> object is created and added to the collection and the <a href="https://msdn.microsoft.com/9050f394-ccad-4a6e-90bc-53af3a874f91">Selected</a> property is set to SelectedNo.</li>
<li>The <a href="https://msdn.microsoft.com/9050f394-ccad-4a6e-90bc-53af3a874f91">Selected</a> property is set to SelectedYes for each CryptoAPI CSP/algorithm pair where the algorithm can be used only to sign data.</li>
<li>The <a href="https://msdn.microsoft.com/e392e28f-084e-43a7-8a5e-14bea0ed8d58">Ordinal</a> property is set to reflect the CSP order, if any, identified by the <b>pKIDefaultCSPs</b> template attribute. The CSPs listed first by the attribute are ordered first in the collection. This property is used during enrollment if a private key must be created. The first selected CSP/algorithm pair is used to create the key, but if the operation fails, the next selected pair is tried.</li>
<li>Calling this method again with the same <i>KeySpec</i> parameter retrieves a pointer to the existing collection created previously for that parameter value.</li>
<li>Calling this method again with a different <i>KeySpec</i> parameter will not affect the collection created for the XCN_AT_SIGNATURE <i>KeySpec</i> value. Further, changing the <a href="https://msdn.microsoft.com/9050f394-ccad-4a6e-90bc-53af3a874f91">Selected</a> property on any member of the new collection does not affect any member of the previous collection.</li>
</ul>


The <b>GetCspStatuses</b> method differs from the <a href="https://msdn.microsoft.com/cad6d8f0-f7d6-4ede-96a2-b00159962a1b">CspStatuses</a> property by use of the <i>KeySpec</i> parameter. The method allows users to specify this value, but the property uses the value set on the private key associated with the request object.

 You must initialize the <a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a> object before calling this method. For more information, see any of the following methods:<ul>
<li>
<a href="https://msdn.microsoft.com/10ab62c3-9c6f-4e1b-8a86-131d08282d9c">InitializeDecode</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3f390abc-5c1c-4f9c-a5f4-4d6fec065acf">InitializeFromCertificate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b26e69c4-bfe4-4395-aaf6-bc1d045f59cc">InitializeFromPrivateKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7b7e00dc-649b-4bcb-a9b6-5745b33ea48b">InitializeFromPublicKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4ea746c3-b967-41b4-94ae-7b16b93ca4e4">InitializeFromTemplateName</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a>
 

 

