---
UID: NF:certenroll.IX509CertificateRequestPkcs10V2.InitializeFromTemplate
title: IX509CertificateRequestPkcs10V2::InitializeFromTemplate
author: windows-sdk-content
description: Initializes the certificate request by using a template.
old-location: security\ix509certificaterequestpkcs10v2_initializefromtemplate.htm
old-project: seccertenroll
ms.assetid: 599b4dfc-43a2-4be5-aa23-d3844ae442aa
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: ContextAdministratorForceMachine, ContextMachine, ContextUser, IX509CertificateRequestPkcs10V2 interface [Security],InitializeFromTemplate method, IX509CertificateRequestPkcs10V2.InitializeFromTemplate, IX509CertificateRequestPkcs10V2::InitializeFromTemplate, InitializeFromTemplate, InitializeFromTemplate method [Security], InitializeFromTemplate method [Security],IX509CertificateRequestPkcs10V2 interface, certenroll/IX509CertificateRequestPkcs10V2::InitializeFromTemplate, security.ix509certificaterequestpkcs10v2_initializefromtemplate
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenroll.h
api_name:
 - IX509CertificateRequestPkcs10V2.InitializeFromTemplate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IX509CertificateRequestPkcs10V2::InitializeFromTemplate


## -description


The <b>InitializeFromTemplate</b> method initializes the certificate request by using a template.


## -parameters




### -param context




### -param pPolicyServer [in]

Pointer to an <a href="https://msdn.microsoft.com/e39d40fd-3d43-4cdc-b41a-07a87a11bfad">IX509EnrollmentPolicyServer</a> object that represents the certificate enrollment policy (CEP) server that contains the template specified by the <i>pTemplate</i> parameter.


### -param pTemplate [in]

Pointer to an <a href="https://msdn.microsoft.com/56122d92-7e38-4eaa-b2f5-713adc81e68e">IX509CertificateTemplate</a> object that represents the template to use during initialization.


#### - Context [in]

An <a href="https://msdn.microsoft.com/2db0e129-a566-47ba-ab57-53c7db09e8e3">X509CertificateEnrollmentContext</a> enumeration value that specifies whether the requested certificate is intended for an end user, a computer, or administrator acting on behalf of the computer. This can be one of the following values. 

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pPolicyServer</i> or <i>pTemplate</i> parameters are <b>NULL</b>.

</td>
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



The <b>InitializeFromTemplate</b> method creates the following collections:<ul>
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
<li>Populates many of the <a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a> properties from the template settings.</li>
</ul>


If the <a href="https://msdn.microsoft.com/7be532ab-0ab0-4c22-b274-c925fd5827d5">CSPInformations</a> property is <b>NULL</b>, the method creates an <a href="https://msdn.microsoft.com/8141023c-c162-46d6-9c37-e227ce1c8761">ICspInformations</a> collection from the providers installed on the computer.




## -see-also




<a href="https://msdn.microsoft.com/38177793-c15b-4651-8260-c90a151da83e">IX509CertificateRequestPkcs10V2</a>
 

 

