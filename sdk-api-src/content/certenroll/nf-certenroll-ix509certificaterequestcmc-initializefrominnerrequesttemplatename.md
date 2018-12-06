---
UID: NF:certenroll.IX509CertificateRequestCmc.InitializeFromInnerRequestTemplateName
title: IX509CertificateRequestCmc::InitializeFromInnerRequestTemplateName
author: windows-sdk-content
description: The InitializeFromInnerRequestTemplateName method initializes the certificate request from an inner request object and a template.
old-location: security\ix509certificaterequestcmc_initializefrominnerrequesttemplatename.htm
tech.root: seccertenroll
ms.assetid: abf7617e-1194-4303-a214-23fbaf20eccf
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IX509CertificateRequestCmc interface [Security],InitializeFromInnerRequestTemplateName method, IX509CertificateRequestCmc.InitializeFromInnerRequestTemplateName, IX509CertificateRequestCmc::InitializeFromInnerRequestTemplateName, InitializeFromInnerRequestTemplateName, InitializeFromInnerRequestTemplateName method [Security], InitializeFromInnerRequestTemplateName method [Security],IX509CertificateRequestCmc interface, certenroll/IX509CertificateRequestCmc::InitializeFromInnerRequestTemplateName, security.ix509certificaterequestcmc_initializefrominnerrequesttemplatename
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
 - IX509CertificateRequestCmc.InitializeFromInnerRequestTemplateName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequestCmc::InitializeFromInnerRequestTemplateName


## -description


The <b>InitializeFromInnerRequestTemplateName</b> method initializes the certificate request from an inner request  object and a template.


## -parameters




### -param pInnerRequest [in]

Pointer to an <a href="https://msdn.microsoft.com/5425c9ab-565d-449d-87e1-e5765868acfb">IX509CertificateRequest</a> interface that represents the inner request object. This can be a PKCS #10 or  a CMC request.


### -param strTemplateName [in]

A <b>BSTR</b> variable that contains the Common Name (CN) of the template as it appears in Active Directory or the dotted decimal <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a>.


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
<dt><b><b>CRYPT_E_INVALID_MSG_TYPE</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The request object passed to the <i>pInnerRequest</i> parameter must be a PKCS #10 or a CMC request.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The request object has already been initialized.

</td>
</tr>
</table>
 




## -remarks



By specifying a template, you can add information to the outer request object that may not be contained in the inner request. For example, if the inner request does not contain the necessary extensions, you can supply a template that does.

The <b>InitializeFromInnerRequestTemplateName</b> method:<ul>
<li>Creates an empty <a href="https://msdn.microsoft.com/beedb57c-1c89-4d16-8514-046e3071fd1e">ICryptAttributes</a> collection.</li>
<li>Creates an empty <a href="https://msdn.microsoft.com/c881dc9f-4187-4ba1-9f3a-e1564e4f37c7">IX509NameValuePairs</a> collection.</li>
<li>Creates an empty <a href="https://msdn.microsoft.com/d6bdbcff-1d6b-4813-8269-b75061a42de8">IX509Extensions</a> collection.</li>
<li>Creates an <a href="https://msdn.microsoft.com/f376a33e-005b-4810-9a26-b642236ff7af">IObjectIds</a> collection for  critical extensions and adds the XCN_OID_KEY_USAGE and XCN_OID_BASIC_CONSTRAINTS2 object identifiers (OIDs).</li>
<li>Creates an empty <a href="https://msdn.microsoft.com/f376a33e-005b-4810-9a26-b642236ff7af">IObjectIds</a> collection of OIDs to be suppressed from the request object.</li>
<li>Creates an empty <a href="https://msdn.microsoft.com/420d6550-514a-4fea-987b-6deecbc9b717">ISignerCertificates</a> collection.</li>
<li>Retrieves private key flags from the template.</li>
<li>Sets the <a href="https://msdn.microsoft.com/6d17222e-3657-4911-a8e7-d90214284441">ArchivePrivateKey</a> property if required by the template flags or settings.</li>
<li>Retrieves the encryption algorithm from the template if one is specified and sets the <a href="https://msdn.microsoft.com/c46b3373-6d9e-46d9-a36a-b73a718ddaf7">EncryptionAlgorithm</a> property.</li>
<li>Sets the <a href="https://msdn.microsoft.com/9cade9f0-d614-4838-bf42-0a19b4ce53d5">EncryptionStrength</a> property if possible.</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/77059388-c442-4db5-ab27-1db25e2f63b9">IX509CertificateRequestCmc</a>
 

 

