---
UID: NF:certenroll.IX509CertificateRequestPkcs10.InitializeFromPrivateKey
title: IX509CertificateRequestPkcs10::InitializeFromPrivateKey
author: windows-sdk-content
description: Initializes the certificate request by using an IX509PrivateKey object and, optionally, a template.
old-location: security\ix509certificaterequestpkcs10_initializefromprivatekey_method.htm
tech.root: seccertenroll
ms.assetid: b26e69c4-bfe4-4395-aaf6-bc1d045f59cc
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: ContextAdministratorForceMachine, ContextMachine, ContextUser, IX509CertificateRequestPkcs10 interface [Security],InitializeFromPrivateKey method, IX509CertificateRequestPkcs10.InitializeFromPrivateKey, IX509CertificateRequestPkcs10::InitializeFromPrivateKey, InitializeFromPrivateKey, InitializeFromPrivateKey method [Security], InitializeFromPrivateKey method [Security],IX509CertificateRequestPkcs10 interface, certenroll/IX509CertificateRequestPkcs10::InitializeFromPrivateKey, security.ix509certificaterequestpkcs10_initializefromprivatekey_method
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
 - IX509CertificateRequestPkcs10.InitializeFromPrivateKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequestPkcs10::InitializeFromPrivateKey


## -description


The <b>InitializeFromPrivateKey</b> method initializes the certificate request by using an <a href="https://msdn.microsoft.com/en-us/library/Aa378921(v=VS.85).aspx">IX509PrivateKey</a> object and, optionally, a template. This method is web enabled.


## -parameters




### -param Context [in]

An <a href="https://msdn.microsoft.com/en-us/library/Aa379399(v=VS.85).aspx">X509CertificateEnrollmentContext</a> enumeration value that specifies whether the requested certificate is intended for an end user, a computer, or an administrator acting on behalf of the computer. This can be one of the following values. However, if the <a href="https://msdn.microsoft.com/en-us/library/Aa379024(v=VS.85).aspx">MachineContext</a> property of the <a href="https://msdn.microsoft.com/en-us/library/ms721603(v=VS.85).aspx">private key</a> is set, you must specify the <b>ContextMachine</b> enumeration value.

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
 


### -param pPrivateKey [in]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Aa378921(v=VS.85).aspx">IX509PrivateKey</a> interface that represents the private key.


### -param strTemplateName [in, optional]

A <b>BSTR</b> variable that contains the Common Name (CN) of the template as it appears in Active Directory or the dotted decimal <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a>. This is an optional parameter.


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
The certificate request object has already been initialized.

</td>
</tr>
</table>
 




## -remarks



If you specify a template, the <b>InitializeFromPrivateKey</b> method performs the following actions:<ul>
<li>Adds the extensions specified by the template to an <a href="https://msdn.microsoft.com/en-us/library/Aa378174(v=VS.85).aspx">IX509Extensions</a> collection.</li>
<li>Creates an <a href="https://msdn.microsoft.com/en-us/library/Aa376785(v=VS.85).aspx">IObjectIds</a> collection and populates it with the default XCN_OID_KEY_USAGE and XCN_OID_BASIC_CONSTRAINTS2 object identifiers. If the template indicates that these OIDs are not critical, they are removed from the collection. The OIDs marked critical by the template are added.</li>
<li>Sets the <a href="https://msdn.microsoft.com/en-us/library/Aa377586(v=VS.85).aspx">SmimeCapabilities</a> property if the template supports symmetric algorithms.</li>
<li>Sets the <a href="https://msdn.microsoft.com/en-us/library/Aa965816(v=VS.85).aspx">AlternateSignatureAlgorithm</a> property if the template requires a discrete signature algorithm OID.</li>
<li>Creates an <a href="https://msdn.microsoft.com/en-us/library/Aa379050(v=VS.85).aspx">IX509SignatureInformation</a> object.</li>
<li>Creates a hash algorithm OID if the algorithm is specified in the template and sets it on the <a href="https://msdn.microsoft.com/en-us/library/Aa379050(v=VS.85).aspx">IX509SignatureInformation</a> object.</li>
<li>Retrieves an asymmetric encryption algorithm OID, if it exists, from the template and sets it on the <a href="https://msdn.microsoft.com/en-us/library/Aa379050(v=VS.85).aspx">IX509SignatureInformation</a> object.</li>
<li>Populates many of the <a href="https://msdn.microsoft.com/en-us/library/Aa378921(v=VS.85).aspx">IX509PrivateKey</a> properties from the template settings.</li>
</ul>


Whether you specify a template or not, if the <a href="https://msdn.microsoft.com/en-us/library/Aa377643(v=VS.85).aspx">CSPInformations</a> property is not specified, the method creates an <a href="https://msdn.microsoft.com/en-us/library/Aa375968(v=VS.85).aspx">ICspInformations</a> collection from the providers installed on the computer.

No private key is created at this point. If the <a href="https://msdn.microsoft.com/en-us/library/Aa378921(v=VS.85).aspx">IX509PrivateKey</a> object passed to the method does not represent an existing key, a key is created when the <a href="https://msdn.microsoft.com/en-us/library/Aa377650(v=VS.85).aspx">Encode</a> method is called. The key will be created by using the default provider if no template was specified and the <a href="https://msdn.microsoft.com/en-us/library/Aa379031(v=VS.85).aspx">ProviderName</a> property on the <b>IX509PrivateKey</b> is not set. When a private key exists, it is set on the <a href="https://msdn.microsoft.com/en-us/library/Aa377559(v=VS.85).aspx">PrivateKey</a> property.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a>
 

 

