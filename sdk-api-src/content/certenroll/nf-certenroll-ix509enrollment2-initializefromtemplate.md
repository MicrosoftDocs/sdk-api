---
UID: NF:certenroll.IX509Enrollment2.InitializeFromTemplate
title: IX509Enrollment2::InitializeFromTemplate (certenroll.h)
description: Initializes the enrollment object by using a template.
helpviewer_keywords: ["ContextAdministratorForceMachine","ContextMachine","ContextUser","IX509Enrollment2 interface [Security]","InitializeFromTemplate method","IX509Enrollment2.InitializeFromTemplate","IX509Enrollment2::InitializeFromTemplate","InitializeFromTemplate","InitializeFromTemplate method [Security]","InitializeFromTemplate method [Security]","IX509Enrollment2 interface","certenroll/IX509Enrollment2::InitializeFromTemplate","security.ix509enrollment2_initializefromtemplate"]
old-location: security\ix509enrollment2_initializefromtemplate.htm
tech.root: security
ms.assetid: aa260ff7-d55b-4fda-88e2-2f1d68cc41e1
ms.date: 12/05/2018
ms.keywords: ContextAdministratorForceMachine, ContextMachine, ContextUser, IX509Enrollment2 interface [Security],InitializeFromTemplate method, IX509Enrollment2.InitializeFromTemplate, IX509Enrollment2::InitializeFromTemplate, InitializeFromTemplate, InitializeFromTemplate method [Security], InitializeFromTemplate method [Security],IX509Enrollment2 interface, certenroll/IX509Enrollment2::InitializeFromTemplate, security.ix509enrollment2_initializefromtemplate
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IX509Enrollment2::InitializeFromTemplate
 - certenroll/IX509Enrollment2::InitializeFromTemplate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenroll.h
api_name:
 - IX509Enrollment2.InitializeFromTemplate
---

# IX509Enrollment2::InitializeFromTemplate


## -description

The <b>InitializeFromTemplate</b> method initializes the enrollment object by using a template.

## -parameters

### -param context [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-x509certificateenrollmentcontext">X509CertificateEnrollmentContext</a> enumeration value that indicates whether the requested enrollment is for a user, a computer, or an administrator acting on behalf of a computer. This can be one of the following values.

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

### -param pPolicyServer [in]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmentpolicyserver">IX509EnrollmentPolicyServer</a> object that represents the certificate enrollment policy (CEP) server that contains the template specified by the <i>pTemplate</i> parameter.

### -param pTemplate [in]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificatetemplate">IX509CertificateTemplate</a> object that represents the template to use during initialization.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

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
The <i>pPolicyServer</i> and <i>pTemplate</i> parameters cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The enrollment object has already been initialized.

</td>
</tr>
</table>

## -remarks

The <b>InitializeFromTemplate</b> method:

<ul>
<li>Examines the template to determine the type of request needed.</li>
<li>Creates the appropriate type of request object (PKCS #10, PKCS #7, or CMC).</li>
<li>Sets the following properties on the request if values currently exist:<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_cspinformations">CspInformations</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_parentwindow">ParentWindow</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_silent">Silent</a>
</li>
</ul>
</li>
<li>Initializes the request object by using the template.</li>
<li>Retrieves the signature count, issuance policies, and application policies from the template.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollment2">IX509Enrollment2</a>