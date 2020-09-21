---
UID: NF:certenroll.IX509PolicyServerUrl.Initialize
title: IX509PolicyServerUrl::Initialize (certenroll.h)
description: Initializes an IX509PolicyServerUrl object for a computer or user context.
helpviewer_keywords: ["ContextAdministratorForceMachine","ContextMachine","ContextUser","IX509PolicyServerUrl interface [Security]","Initialize method","IX509PolicyServerUrl.Initialize","IX509PolicyServerUrl::Initialize","Initialize","Initialize method [Security]","Initialize method [Security]","IX509PolicyServerUrl interface","certenroll/IX509PolicyServerUrl::Initialize","security.ix509policyserverurl_initialize"]
old-location: security\ix509policyserverurl_initialize.htm
tech.root: security
ms.assetid: 693c3a29-0d12-4603-a06a-4277db3b8b8b
ms.date: 12/05/2018
ms.keywords: ContextAdministratorForceMachine, ContextMachine, ContextUser, IX509PolicyServerUrl interface [Security],Initialize method, IX509PolicyServerUrl.Initialize, IX509PolicyServerUrl::Initialize, Initialize, Initialize method [Security], Initialize method [Security],IX509PolicyServerUrl interface, certenroll/IX509PolicyServerUrl::Initialize, security.ix509policyserverurl_initialize
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
 - IX509PolicyServerUrl::Initialize
 - certenroll/IX509PolicyServerUrl::Initialize
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
 - IX509PolicyServerUrl.Initialize
---

# IX509PolicyServerUrl::Initialize


## -description

The <b>Initialize</b> method initializes an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509policyserverurl">IX509PolicyServerUrl</a> object for a computer or user context.

## -parameters

### -param context [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-x509certificateenrollmentcontext">X509CertificateEnrollmentContext</a> enumeration value that specifies the nature of the end entity for which an issued certificate is intended. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ContextUser"></a><a id="contextuser"></a><a id="CONTEXTUSER"></a><dl>
<dt><b>ContextUser</b></dt>
</dl>
</td>
<td width="60%">
The certificate is intended for an end user.

</td>
</tr>
<tr>
<td width="40%"><a id="ContextMachine"></a><a id="contextmachine"></a><a id="CONTEXTMACHINE"></a><dl>
<dt><b>ContextMachine</b></dt>
</dl>
</td>
<td width="60%">
The certificate is intended for a computer.

</td>
</tr>
<tr>
<td width="40%"><a id="ContextAdministratorForceMachine"></a><a id="contextadministratorforcemachine"></a><a id="CONTEXTADMINISTRATORFORCEMACHINE"></a><dl>
<dt><b>ContextAdministratorForceMachine</b></dt>
</dl>
</td>
<td width="60%">
The certificate is being requested by an administrator acting on the behalf of a computer.

</td>
</tr>
</table>

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

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
The <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509policyserverurl">IX509PolicyServerUrl</a> has already been initialized.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509policyserverurl">IX509PolicyServerUrl</a>