---
UID: NF:certenroll.IX509PolicyServerListManager.Initialize
title: IX509PolicyServerListManager::Initialize (certenroll.h)
description: Initializes an IX509PolicyServerListManager object.
helpviewer_keywords: ["ContextAdministratorForceMachine","ContextMachine","ContextUser","IX509PolicyServerListManager interface [Security]","Initialize method","IX509PolicyServerListManager.Initialize","IX509PolicyServerListManager::Initialize","Initialize","Initialize method [Security]","Initialize method [Security]","IX509PolicyServerListManager interface","PsfLocationGroupPolicy","PsfLocationRegistry","certenroll/IX509PolicyServerListManager::Initialize","security.ix509policyserverlistmanager_initialize"]
old-location: security\ix509policyserverlistmanager_initialize.htm
tech.root: security
ms.assetid: 9b3d2913-a0a8-4ec0-b705-8525b54e5494
ms.date: 12/05/2018
ms.keywords: ContextAdministratorForceMachine, ContextMachine, ContextUser, IX509PolicyServerListManager interface [Security],Initialize method, IX509PolicyServerListManager.Initialize, IX509PolicyServerListManager::Initialize, Initialize, Initialize method [Security], Initialize method [Security],IX509PolicyServerListManager interface, PsfLocationGroupPolicy, PsfLocationRegistry, certenroll/IX509PolicyServerListManager::Initialize, security.ix509policyserverlistmanager_initialize
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IX509PolicyServerListManager::Initialize
 - certenroll/IX509PolicyServerListManager::Initialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509PolicyServerListManager.Initialize
---

# IX509PolicyServerListManager::Initialize


## -description

The <b>Initialize</b> method initializes an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509policyserverlistmanager">IX509PolicyServerListManager</a> object.

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

### -param Flags [in]

A <a href="/windows/desktop/api/certenroll/ne-certenroll-policyserverurlflags">PolicyServerUrlFlags</a> enumeration value that specifies where policy information is located. This can be a bitwise <b>OR</b> of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PsfLocationGroupPolicy"></a><a id="psflocationgrouppolicy"></a><a id="PSFLOCATIONGROUPPOLICY"></a><dl>
<dt><b>PsfLocationGroupPolicy</b></dt>
</dl>
</td>
<td width="60%">
Policy information is specified in group policy by an administrator.

</td>
</tr>
<tr>
<td width="40%"><a id="PsfLocationRegistry"></a><a id="psflocationregistry"></a><a id="PSFLOCATIONREGISTRY"></a><dl>
<dt><b>PsfLocationRegistry</b></dt>
</dl>
</td>
<td width="60%">
Policy information is specified in the registry.

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
The <i>Flags</i> parameter must contain a bitwise OR of <b>PsfLocationGroupPolicy</b> and <b>PsfLocationRegistry</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509policyserverlistmanager">IX509PolicyServerListManager</a> has already been initialized.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509policyserverlistmanager">IX509PolicyServerListManager</a>