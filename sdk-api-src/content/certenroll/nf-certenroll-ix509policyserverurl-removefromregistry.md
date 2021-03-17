---
UID: NF:certenroll.IX509PolicyServerUrl.RemoveFromRegistry
title: IX509PolicyServerUrl::RemoveFromRegistry (certenroll.h)
description: Unregisters a certificate enrollment policy (CEP) server.
helpviewer_keywords: ["ContextAdministratorForceMachine","ContextMachine","ContextUser","IX509PolicyServerUrl interface [Security]","RemoveFromRegistry method","IX509PolicyServerUrl.RemoveFromRegistry","IX509PolicyServerUrl::RemoveFromRegistry","RemoveFromRegistry","RemoveFromRegistry method [Security]","RemoveFromRegistry method [Security]","IX509PolicyServerUrl interface","certenroll/IX509PolicyServerUrl::RemoveFromRegistry","security.ix509policyserverurl_removefromregistry"]
old-location: security\ix509policyserverurl_removefromregistry.htm
tech.root: security
ms.assetid: 18f9a445-99db-43b1-bee0-35bfbd1de0a5
ms.date: 12/05/2018
ms.keywords: ContextAdministratorForceMachine, ContextMachine, ContextUser, IX509PolicyServerUrl interface [Security],RemoveFromRegistry method, IX509PolicyServerUrl.RemoveFromRegistry, IX509PolicyServerUrl::RemoveFromRegistry, RemoveFromRegistry, RemoveFromRegistry method [Security], RemoveFromRegistry method [Security],IX509PolicyServerUrl interface, certenroll/IX509PolicyServerUrl::RemoveFromRegistry, security.ix509policyserverurl_removefromregistry
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
 - IX509PolicyServerUrl::RemoveFromRegistry
 - certenroll/IX509PolicyServerUrl::RemoveFromRegistry
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
 - IX509PolicyServerUrl.RemoveFromRegistry
---

# IX509PolicyServerUrl::RemoveFromRegistry


## -description

The <b>RemoveFromRegistry</b> method unregisters a certificate enrollment policy (CEP) server.

## -parameters

### -param context [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-x509certificateenrollmentcontext">X509CertificateEnrollmentContext</a> enumeration value that specifies the nature of the end entity. This can be one of the following values.

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
<dt><b>HRESULT_FROM_WIN32(ERROR_ACCESS_DISABLED_BY_POLICY)</b></dt>
</dl>
</td>
<td width="60%">
You do not have sufficient access rights to unregister the CEP.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509policyserverurl">IX509PolicyServerUrl</a>