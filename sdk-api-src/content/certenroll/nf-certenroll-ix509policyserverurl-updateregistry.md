---
UID: NF:certenroll.IX509PolicyServerUrl.UpdateRegistry
title: IX509PolicyServerUrl::UpdateRegistry (certenroll.h)
description: Registers a certificate enrollment policy (CEP) server.
helpviewer_keywords: ["ContextAdministratorForceMachine","ContextMachine","ContextUser","IX509PolicyServerUrl interface [Security]","UpdateRegistry method","IX509PolicyServerUrl.UpdateRegistry","IX509PolicyServerUrl::UpdateRegistry","UpdateRegistry","UpdateRegistry method [Security]","UpdateRegistry method [Security]","IX509PolicyServerUrl interface","certenroll/IX509PolicyServerUrl::UpdateRegistry","security.ix509policyserverurl_updateregistry"]
old-location: security\ix509policyserverurl_updateregistry.htm
tech.root: security
ms.assetid: dfb43979-a630-497d-96eb-f2bd701b5e09
ms.date: 12/05/2018
ms.keywords: ContextAdministratorForceMachine, ContextMachine, ContextUser, IX509PolicyServerUrl interface [Security],UpdateRegistry method, IX509PolicyServerUrl.UpdateRegistry, IX509PolicyServerUrl::UpdateRegistry, UpdateRegistry, UpdateRegistry method [Security], UpdateRegistry method [Security],IX509PolicyServerUrl interface, certenroll/IX509PolicyServerUrl::UpdateRegistry, security.ix509policyserverurl_updateregistry
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
 - IX509PolicyServerUrl::UpdateRegistry
 - certenroll/IX509PolicyServerUrl::UpdateRegistry
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
 - IX509PolicyServerUrl.UpdateRegistry
---

# IX509PolicyServerUrl::UpdateRegistry


## -description

The <b>UpdateRegistry</b> method registers a certificate enrollment policy (CEP) server.

## -parameters

### -param context [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-x509certificateenrollmentcontext">X509CertificateEnrollmentContext</a> enumeration value that specifies the nature of the end entity for which the policy server is being registered. This can be one of the following values.

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
An end user.

</td>
</tr>
<tr>
<td width="40%"><a id="ContextMachine"></a><a id="contextmachine"></a><a id="CONTEXTMACHINE"></a><dl>
<dt><b>ContextMachine</b></dt>
</dl>
</td>
<td width="60%">
A computer.

</td>
</tr>
<tr>
<td width="40%"><a id="ContextAdministratorForceMachine"></a><a id="contextadministratorforcemachine"></a><a id="CONTEXTADMINISTRATORFORCEMACHINE"></a><dl>
<dt><b>ContextAdministratorForceMachine</b></dt>
</dl>
</td>
<td width="60%">
An administrator acting on the behalf of a computer.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The URL of the policy server is empty.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_ACCESS_DISABLED_BY_POLICY)</b></dt>
</dl>
</td>
<td width="60%">
You do not have sufficient access rights to register the CEP.

</td>
</tr>
</table>

## -remarks

The <b>UpdateRegistry</b> method is called by the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmenthelper-addpolicyserver">AddPolicyServer</a> method.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509policyserverurl">IX509PolicyServerUrl</a>