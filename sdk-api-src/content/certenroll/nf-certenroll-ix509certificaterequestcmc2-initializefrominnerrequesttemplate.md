---
UID: NF:certenroll.IX509CertificateRequestCmc2.InitializeFromInnerRequestTemplate
title: IX509CertificateRequestCmc2::InitializeFromInnerRequestTemplate (certenroll.h)
author: windows-sdk-content
description: Initializes the certificate request from an inner request object and a template.
old-location: security\ix509certificaterequestcmc2_initializefrominnerrequesttemplate.htm
tech.root: seccertenroll
ms.assetid: 12490859-bb4a-49ff-9d92-24bf04ab3999
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestCmc2 interface [Security],InitializeFromInnerRequestTemplate method, IX509CertificateRequestCmc2.InitializeFromInnerRequestTemplate, IX509CertificateRequestCmc2::InitializeFromInnerRequestTemplate, InitializeFromInnerRequestTemplate, InitializeFromInnerRequestTemplate method [Security], InitializeFromInnerRequestTemplate method [Security],IX509CertificateRequestCmc2 interface, certenroll/IX509CertificateRequestCmc2::InitializeFromInnerRequestTemplate, security.ix509certificaterequestcmc2_initializefrominnerrequesttemplate
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certenroll.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenroll.h
api_name:
 - IX509CertificateRequestCmc2.InitializeFromInnerRequestTemplate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequestCmc2::InitializeFromInnerRequestTemplate


## -description


The <b>InitializeFromInnerRequestTemplate</b> method initializes the certificate request from an inner request  object and a template.


## -parameters




### -param pInnerRequest [in]

Pointer to an <a href="https://msdn.microsoft.com/5425c9ab-565d-449d-87e1-e5765868acfb">IX509CertificateRequest</a> interface that represents the inner request object. This can be a PKCS #10 or  a CMC request.


### -param pPolicyServer [in]

Pointer to an <a href="https://msdn.microsoft.com/e39d40fd-3d43-4cdc-b41a-07a87a11bfad">IX509EnrollmentPolicyServer</a> object that represents the certificate enrollment policy (CEP) server that contains the template specified by the <i>pTemplate</i> parameter.


### -param pTemplate [in]

Pointer to an <a href="https://msdn.microsoft.com/56122d92-7e38-4eaa-b2f5-713adc81e68e">IX509CertificateTemplate</a> object that represents the template to use during initialization.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pInnerRequest</i>, <i>pPolicyServer</i>, and <i>pTemplate</i> parameters cannot be <b>NULL</b>.

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

The <b>InitializeFromInnerRequestTemplate</b> method:<ul>
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




<a href="https://msdn.microsoft.com/27edf846-472e-4a22-bd3c-88044a1fbd99">IX509CertificateRequestCmc2</a>
 

 

