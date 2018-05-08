---
UID: NF:certenroll.IX509CertificateRequest.Initialize
title: IX509CertificateRequest::Initialize
author: windows-driver-content
description: Initializes the request object for a user or a computer.
old-location: security\ix509certificaterequest_initialize_method.htm
old-project: SecCertEnroll
ms.assetid: be0e2cda-5481-49ab-9a12-6dc52981fd24
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: ContextAdministratorForceMachine, ContextMachine, ContextUser, IX509CertificateRequest interface [Security],Initialize method, IX509CertificateRequest.Initialize, IX509CertificateRequest::Initialize, Initialize, Initialize method [Security], Initialize method [Security],IX509CertificateRequest interface, certenroll/IX509CertificateRequest::Initialize, security.ix509certificaterequest_initialize_method
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	IX509CertificateRequest.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequest::Initialize


## -description


The <b>Initialize</b> method initializes the request object for a user or a computer.


## -parameters




### -param Context [in]

An <a href="https://msdn.microsoft.com/2db0e129-a566-47ba-ab57-53c7db09e8e3">X509CertificateEnrollmentContext</a> enumeration value that specifies whether the certificate is intended for an end user, a computer, or an administrator acting on behalf of a computer. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ContextUser"></a><a id="contextuser"></a><a id="CONTEXTUSER"></a><dl>
<dt><b>ContextUser</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The certificate is being requested for an end user.

</td>
</tr>
<tr>
<td width="40%"><a id="ContextMachine"></a><a id="contextmachine"></a><a id="CONTEXTMACHINE"></a><dl>
<dt><b>ContextMachine</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The certificate is being requested for a computer.

</td>
</tr>
<tr>
<td width="40%"><a id="ContextAdministratorForceMachine"></a><a id="contextadministratorforcemachine"></a><a id="CONTEXTADMINISTRATORFORCEMACHINE"></a><dl>
<dt><b>ContextAdministratorForceMachine</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The certificate is being requested by an administrator acting on the behalf of a computer.

</td>
</tr>
</table>
 


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
<dt><b>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</b></dt>
</dl>
</td>
<td width="60%">
The object is already initialized.

</td>
</tr>
</table>
 




## -remarks



The  <b>Initialize</b> method initializes various objects depending on the type of certificate request being created. If you call this method from an <a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a> object, a private key object is created and the following objects are initialized:<ul>
<li>An empty <a href="https://msdn.microsoft.com/beedb57c-1c89-4d16-8514-046e3071fd1e">ICryptAttributes</a> collection.</li>
<li>An empty <a href="https://msdn.microsoft.com/d6bdbcff-1d6b-4813-8269-b75061a42de8">IX509Extensions</a> collection.</li>
<li>An <a href="https://msdn.microsoft.com/f376a33e-005b-4810-9a26-b642236ff7af">IObjectIds</a> collection that contains the default critical extension object identifiers, XCN_OID_KEY_USAGE and XCN_OID_BASIC_CONSTRAINTS2. This collection can be retrieved by calling the <a href="https://msdn.microsoft.com/7ecde7cb-1a73-4fee-a949-c4bb36e61547">CriticalExtensions</a> property.</li>
<li>An empty <a href="https://msdn.microsoft.com/f376a33e-005b-4810-9a26-b642236ff7af">IObjectIds</a> collection for the <a href="https://msdn.microsoft.com/3f7a6d23-00d3-4ab6-817a-a37490f0cb84">SuppressOids</a> property.</li>
<li>An <a href="https://msdn.microsoft.com/8141023c-c162-46d6-9c37-e227ce1c8761">ICspInformations</a> object that contains the values you specified in the <a href="https://msdn.microsoft.com/7be532ab-0ab0-4c22-b274-c925fd5827d5">CSPInformations</a> property or a collection of all providers installed on the computer. This collection is used to create a private key.</li>
</ul>


If you call this method from an <a href="https://msdn.microsoft.com/77059388-c442-4db5-ab27-1db25e2f63b9">IX509CertificateRequestCmc</a> object, an inner PKCS #10 request is created as above and the following objects are initialized:<ul>
<li>An empty <a href="https://msdn.microsoft.com/beedb57c-1c89-4d16-8514-046e3071fd1e">ICryptAttributes</a> collection.</li>
<li>An empty <a href="https://msdn.microsoft.com/c881dc9f-4187-4ba1-9f3a-e1564e4f37c7">IX509NameValuePairs</a> collection.</li>
<li>An empty <a href="https://msdn.microsoft.com/d6bdbcff-1d6b-4813-8269-b75061a42de8">IX509Extensions</a> collection.</li>
<li>An <a href="https://msdn.microsoft.com/f376a33e-005b-4810-9a26-b642236ff7af">IObjectIds</a> collection that contains the default critical extension object identifiers, XCN_OID_KEY_USAGE and XCN_OID_BASIC_CONSTRAINTS2. This collection can be retrieved by calling the <a href="https://msdn.microsoft.com/06c5d148-eecc-45db-9d82-ec56c226ffed">CriticalExtensions</a> property.</li>
<li>An empty IObjectIds collection for the <a href="https://msdn.microsoft.com/6e0a8245-1bcc-413a-865a-8a6274dd55f5">SuppressOids</a> property.</li>
<li>An empty <a href="https://msdn.microsoft.com/420d6550-514a-4fea-987b-6deecbc9b717">ISignerCertificates</a> collection.</li>
</ul>


If you call this method from an <a href="https://msdn.microsoft.com/ae869557-6523-4387-835e-c9631898d864">IX509CertificateRequestPkcs7</a> object, an inner PKCS #10 request is created as above.

The following properties can be called before you call this method. <ul>
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


You must call the <a href="https://msdn.microsoft.com/7be532ab-0ab0-4c22-b274-c925fd5827d5">CSPInformations</a> property before calling this method if you want to specify an <a href="https://msdn.microsoft.com/8141023c-c162-46d6-9c37-e227ce1c8761">ICspInformations</a> collection.




## -see-also




<a href="https://msdn.microsoft.com/5425c9ab-565d-449d-87e1-e5765868acfb">IX509CertificateRequest</a>



<a href="https://msdn.microsoft.com/7197a225-b2dc-47bb-8843-d3fb4bf95811">IX509CertificateRequestCertificate</a>



<a href="https://msdn.microsoft.com/77059388-c442-4db5-ab27-1db25e2f63b9">IX509CertificateRequestCmc</a>



<a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a>



<a href="https://msdn.microsoft.com/ae869557-6523-4387-835e-c9631898d864">IX509CertificateRequestPkcs7</a>



<a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a>
 

 

