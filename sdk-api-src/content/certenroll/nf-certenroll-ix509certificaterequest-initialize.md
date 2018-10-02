---
UID: NF:certenroll.IX509CertificateRequest.Initialize
title: IX509CertificateRequest::Initialize
author: windows-sdk-content
description: Initializes the request object for a user or a computer.
old-location: security\ix509certificaterequest_initialize_method.htm
tech.root: SecCertEnroll
ms.assetid: be0e2cda-5481-49ab-9a12-6dc52981fd24
ms.author: windowssdkdev
ms.date: 09/26/2018
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
 - IX509CertificateRequest.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequest::Initialize


## -description


The <b>Initialize</b> method initializes the request object for a user or a computer.


## -parameters




### -param Context [in]

An <a href="https://msdn.microsoft.com/en-us/library/Aa379399(v=VS.85).aspx">X509CertificateEnrollmentContext</a> enumeration value that specifies whether the certificate is intended for an end user, a computer, or an administrator acting on behalf of a computer. This can be one of the following values.

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

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

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



The  <b>Initialize</b> method initializes various objects depending on the type of certificate request being created. If you call this method from an <a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a> object, a private key object is created and the following objects are initialized:<ul>
<li>An empty <a href="https://msdn.microsoft.com/en-us/library/Aa375930(v=VS.85).aspx">ICryptAttributes</a> collection.</li>
<li>An empty <a href="https://msdn.microsoft.com/en-us/library/Aa378174(v=VS.85).aspx">IX509Extensions</a> collection.</li>
<li>An <a href="https://msdn.microsoft.com/en-us/library/Aa376785(v=VS.85).aspx">IObjectIds</a> collection that contains the default critical extension object identifiers, XCN_OID_KEY_USAGE and XCN_OID_BASIC_CONSTRAINTS2. This collection can be retrieved by calling the <a href="https://msdn.microsoft.com/en-us/library/Aa377513(v=VS.85).aspx">CriticalExtensions</a> property.</li>
<li>An empty <a href="https://msdn.microsoft.com/en-us/library/Aa376785(v=VS.85).aspx">IObjectIds</a> collection for the <a href="https://msdn.microsoft.com/en-us/library/Aa377596(v=VS.85).aspx">SuppressOids</a> property.</li>
<li>An <a href="https://msdn.microsoft.com/en-us/library/Aa375968(v=VS.85).aspx">ICspInformations</a> object that contains the values you specified in the <a href="https://msdn.microsoft.com/en-us/library/Aa377643(v=VS.85).aspx">CSPInformations</a> property or a collection of all providers installed on the computer. This collection is used to create a private key.</li>
</ul>


If you call this method from an <a href="https://msdn.microsoft.com/en-us/library/Aa377133(v=VS.85).aspx">IX509CertificateRequestCmc</a> object, an inner PKCS #10 request is created as above and the following objects are initialized:<ul>
<li>An empty <a href="https://msdn.microsoft.com/en-us/library/Aa375930(v=VS.85).aspx">ICryptAttributes</a> collection.</li>
<li>An empty <a href="https://msdn.microsoft.com/en-us/library/Aa378746(v=VS.85).aspx">IX509NameValuePairs</a> collection.</li>
<li>An empty <a href="https://msdn.microsoft.com/en-us/library/Aa378174(v=VS.85).aspx">IX509Extensions</a> collection.</li>
<li>An <a href="https://msdn.microsoft.com/en-us/library/Aa376785(v=VS.85).aspx">IObjectIds</a> collection that contains the default critical extension object identifiers, XCN_OID_KEY_USAGE and XCN_OID_BASIC_CONSTRAINTS2. This collection can be retrieved by calling the <a href="https://msdn.microsoft.com/en-us/library/Aa377135(v=VS.85).aspx">CriticalExtensions</a> property.</li>
<li>An empty IObjectIds collection for the <a href="https://msdn.microsoft.com/en-us/library/Aa377491(v=VS.85).aspx">SuppressOids</a> property.</li>
<li>An empty <a href="https://msdn.microsoft.com/en-us/library/Aa376821(v=VS.85).aspx">ISignerCertificates</a> collection.</li>
</ul>


If you call this method from an <a href="https://msdn.microsoft.com/en-us/library/Aa377608(v=VS.85).aspx">IX509CertificateRequestPkcs7</a> object, an inner PKCS #10 request is created as above.

The following properties can be called before you call this method. <ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377677(v=VS.85).aspx">ParentWindow</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377696(v=VS.85).aspx">Silent</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377806(v=VS.85).aspx">UIContextMessage</a>
</li>
</ul>


You must call the <a href="https://msdn.microsoft.com/en-us/library/Aa377643(v=VS.85).aspx">CSPInformations</a> property before calling this method if you want to specify an <a href="https://msdn.microsoft.com/en-us/library/Aa375968(v=VS.85).aspx">ICspInformations</a> collection.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377123(v=VS.85).aspx">IX509CertificateRequest</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377124(v=VS.85).aspx">IX509CertificateRequestCertificate</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377133(v=VS.85).aspx">IX509CertificateRequestCmc</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377608(v=VS.85).aspx">IX509CertificateRequestPkcs7</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa379050(v=VS.85).aspx">IX509SignatureInformation</a>
 

 

