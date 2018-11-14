---
UID: NF:certenroll.IX509CertificateRequestCertificate2.InitializeFromTemplate
title: IX509CertificateRequestCertificate2::InitializeFromTemplate
author: windows-sdk-content
description: Initializes the certificate request by using a template.
old-location: security\ix509certificaterequestcertificate2_initializefromtemplate.htm
tech.root: SecCertEnroll
ms.assetid: bd38413f-9e3d-4d04-8de2-5eb0b637c41c
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ContextAdministratorForceMachine, ContextMachine, ContextUser, IX509CertificateRequestCertificate2 interface [Security],InitializeFromTemplate method, IX509CertificateRequestCertificate2.InitializeFromTemplate, IX509CertificateRequestCertificate2::InitializeFromTemplate, InitializeFromTemplate, InitializeFromTemplate method [Security], InitializeFromTemplate method [Security],IX509CertificateRequestCertificate2 interface, certenroll/IX509CertificateRequestCertificate2::InitializeFromTemplate, security.ix509certificaterequestcertificate2_initializefromtemplate
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
 - IX509CertificateRequestCertificate2.InitializeFromTemplate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- certenroll.h
: 
- IX509CertificateRequestCertificate2.InitializeFromTemplate
: 
---

# IX509CertificateRequestCertificate2::InitializeFromTemplate


## -description


The <b>InitializeFromTemplate</b> method initializes the certificate request by using a template.


## -parameters




### -param context

TBD


### -param pPolicyServer [in]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Ee351692(v=VS.85).aspx">IX509EnrollmentPolicyServer</a> object that represents the certificate enrollment policy (CEP) server that contains the template specified by the <i>pTemplate</i> parameter.


### -param pTemplate [in]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Ee351664(v=VS.85).aspx">IX509CertificateTemplate</a> object that represents the template to use during initialization.


#### - Context [in]

An <a href="https://msdn.microsoft.com/en-us/library/Aa379399(v=VS.85).aspx">X509CertificateEnrollmentContext</a> enumeration value that specifies whether the requested certificate is intended for an end user, a computer, or administrator acting on behalf of the computer. This can be one of the following values. 

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pTemplate</i> parameters cannot be <b>NULL</b>.

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
<li>An <a href="https://msdn.microsoft.com/en-us/library/Aa375930(v=VS.85).aspx">ICryptAttributes</a> collection.</li>
<li>An <a href="https://msdn.microsoft.com/en-us/library/Aa378174(v=VS.85).aspx">IX509Extensions</a> collection.</li>
<li>An <a href="https://msdn.microsoft.com/en-us/library/Aa376785(v=VS.85).aspx">IObjectIds</a> collection populated with the default XCN_OID_KEY_USAGE and XCN_OID_BASIC_CONSTRAINTS2 object identifiers.</li>
<li>An empty <a href="https://msdn.microsoft.com/en-us/library/Aa376785(v=VS.85).aspx">IObjectIds</a> collection for attribute and extension OIDs to be suppressed from the new request.</li>
</ul>


The method then examines the template and performs the following actions:<ul>
<li>Adds the extensions specified by the template to the <a href="https://msdn.microsoft.com/en-us/library/Aa378174(v=VS.85).aspx">IX509Extensions</a> collection.</li>
<li>Removes the default critical extensions (XCN_OID_KEY_USAGE and XCN_OID_BASIC_CONSTRAINTS2) from the collection if the template indicates that they are not critical. The OIDs marked critical by the template are added.</li>
<li>Sets the <a href="https://msdn.microsoft.com/en-us/library/Aa377586(v=VS.85).aspx">SmimeCapabilities</a> property if the template supports symmetric algorithms.</li>
<li>Sets the <a href="https://msdn.microsoft.com/en-us/library/Aa965816(v=VS.85).aspx">AlternateSignatureAlgorithm</a> property if the template requires a discrete signature algorithm OID.</li>
<li>Creates an <a href="https://msdn.microsoft.com/en-us/library/Aa379050(v=VS.85).aspx">IX509SignatureInformation</a> object.</li>
<li>Creates a hash algorithm OID if the algorithm is specified in the template and sets it on the <a href="https://msdn.microsoft.com/en-us/library/Aa379050(v=VS.85).aspx">IX509SignatureInformation</a> object.</li>
<li>Creates an asymmetric encryption algorithm OID if the algorithm is specified in the template and sets it on the <a href="https://msdn.microsoft.com/en-us/library/Aa379050(v=VS.85).aspx">IX509SignatureInformation</a> object.</li>
<li>Populates many of the <a href="https://msdn.microsoft.com/en-us/library/Aa378921(v=VS.85).aspx">IX509PrivateKey</a> properties from the template settings.</li>
</ul>


If the <a href="https://msdn.microsoft.com/en-us/library/Aa377643(v=VS.85).aspx">CSPInformations</a> property is <b>NULL</b>, the method creates an <a href="https://msdn.microsoft.com/en-us/library/Aa375968(v=VS.85).aspx">ICspInformations</a> collection from the providers installed on the computer.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ee351612(v=VS.85).aspx">IX509CertificateRequestCertificate2</a>
 

 

