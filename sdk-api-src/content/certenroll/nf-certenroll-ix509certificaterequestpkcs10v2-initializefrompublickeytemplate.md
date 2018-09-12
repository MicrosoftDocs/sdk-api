---
UID: NF:certenroll.IX509CertificateRequestPkcs10V2.InitializeFromPublicKeyTemplate
title: IX509CertificateRequestPkcs10V2::InitializeFromPublicKeyTemplate
author: windows-sdk-content
description: Initializes a null-signed certificate request by using an IX509PublicKey object and a template.
old-location: security\ix509certificaterequestpkcs10v2_initializefrompublickeytemplate.htm
tech.root: SecCertEnroll
ms.assetid: 20e94948-1455-46c4-bc8c-55dfde45818c
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ContextAdministratorForceMachine, ContextMachine, ContextUser, IX509CertificateRequestPkcs10V2 interface [Security],InitializeFromPublicKeyTemplate method, IX509CertificateRequestPkcs10V2.InitializeFromPublicKeyTemplate, IX509CertificateRequestPkcs10V2::InitializeFromPublicKeyTemplate, InitializeFromPublicKeyTemplate, InitializeFromPublicKeyTemplate method [Security], InitializeFromPublicKeyTemplate method [Security],IX509CertificateRequestPkcs10V2 interface, certenroll/IX509CertificateRequestPkcs10V2::InitializeFromPublicKeyTemplate, security.ix509certificaterequestpkcs10v2_initializefrompublickeytemplate
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IX509CertificateRequestPkcs10V2.InitializeFromPublicKeyTemplate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequestPkcs10V2::InitializeFromPublicKeyTemplate


## -description


The <b>InitializeFromPublicKeyTemplate</b> method initializes a null-signed certificate request by using an <a href="https://msdn.microsoft.com/cd6f28a3-9998-40d7-a3e8-dab0cf3991a8">IX509PublicKey</a> object and a template.


## -parameters




### -param Context [in]

An <a href="https://msdn.microsoft.com/2db0e129-a566-47ba-ab57-53c7db09e8e3">X509CertificateEnrollmentContext</a> enumeration value that specifies whether the requested certificate is intended for an end user, a computer, or an administrator acting on behalf of the computer. This can be one of the following values.

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
 


### -param pPublicKey [in]

Pointer to an <a href="https://msdn.microsoft.com/cd6f28a3-9998-40d7-a3e8-dab0cf3991a8">IX509PublicKey</a> interface that represents the public key.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pPublicKey</i>, <i>pPolicyServer</i>, or <i>pTemplate</i> parameters are <b>NULL</b>.

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
The certificate request object has already been initialized.

</td>
</tr>
</table>
 




## -remarks



The <b>InitializeFromPublicKeyTemplate</b> method performs the following actions:<ul>
<li>Adds the extensions specified in the template, if any, to the <a href="https://msdn.microsoft.com/d6bdbcff-1d6b-4813-8269-b75061a42de8">IX509Extensions</a> collection.</li>
<li>Creates a <a href="https://msdn.microsoft.com/7ecde7cb-1a73-4fee-a949-c4bb36e61547">CriticalExtensions</a> collection and populates it with the default XCN_OID_KEY_USAGE and XCN_OID_BASIC_CONSTRAINTS2 object identifiers. If the template indicates that these OIDs are not critical, they are removed from the collection. The OIDs marked critical by the template, if any,  are added.</li>
<li>Sets the <a href="https://msdn.microsoft.com/5aa027d7-3c31-4b70-92a5-d15d2c410366">SmimeCapabilities</a> property if the template supports symmetric algorithms.</li>
<li>Sets the <a href="https://msdn.microsoft.com/57a87aab-1e53-4b0b-a7b9-2fe89083819b">AlternateSignatureAlgorithm</a> property if the template requires a discrete signature algorithm OID.</li>
<li>Creates an <a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a> object.</li>
<li>Creates a hash algorithm OID if the algorithm is specified in the template and sets it on the <a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a> object.</li>
<li>Creates an asymmetric encryption algorithm OID if the algorithm is specified in the template and sets it on the <a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a> object.</li>
</ul>


If the <a href="https://msdn.microsoft.com/7be532ab-0ab0-4c22-b274-c925fd5827d5">CSPInformations</a> property is not specified, the method creates an <a href="https://msdn.microsoft.com/8141023c-c162-46d6-9c37-e227ce1c8761">ICspInformations</a> collection from the providers installed on the computer.

The method does not create a private key. The use of this method implies that the request is null-signed. Therefore, the method sets the <a href="https://msdn.microsoft.com/a693343e-7c9a-4967-b46c-53936497662a">NullSigned</a> property on the  <a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a> object.




## -see-also




<a href="https://msdn.microsoft.com/38177793-c15b-4651-8260-c90a151da83e">IX509CertificateRequestPkcs10V2</a>
 

 

