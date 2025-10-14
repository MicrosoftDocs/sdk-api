---
UID: NF:certenroll.ICertPropertyEnrollmentPolicyServer.GetUrlFlags
title: ICertPropertyEnrollmentPolicyServer::GetUrlFlags (certenroll.h)
description: Retrieves a set of flags that contain miscellaneous policy information about the certificate enrollment policy (CEP) server.
helpviewer_keywords: ["GetUrlFlags","GetUrlFlags method [Security]","GetUrlFlags method [Security]","ICertPropertyEnrollmentPolicyServer interface","ICertPropertyEnrollmentPolicyServer interface [Security]","GetUrlFlags method","ICertPropertyEnrollmentPolicyServer.GetUrlFlags","ICertPropertyEnrollmentPolicyServer::GetUrlFlags","PsfAllowUnTrustedCA","PsfAutoEnrollmentEnabled","PsfLocationGroupPolicy","PsfLocationRegistry","PsfNone","PsfUseClientId","certenroll/ICertPropertyEnrollmentPolicyServer::GetUrlFlags","security.icertpropertyenrollmentpolicyserver_geturlflags"]
old-location: security\icertpropertyenrollmentpolicyserver_geturlflags.htm
tech.root: security
ms.assetid: eafd4290-5eef-432f-908c-0640a4ac667f
ms.date: 12/05/2018
ms.keywords: GetUrlFlags, GetUrlFlags method [Security], GetUrlFlags method [Security],ICertPropertyEnrollmentPolicyServer interface, ICertPropertyEnrollmentPolicyServer interface [Security],GetUrlFlags method, ICertPropertyEnrollmentPolicyServer.GetUrlFlags, ICertPropertyEnrollmentPolicyServer::GetUrlFlags, PsfAllowUnTrustedCA, PsfAutoEnrollmentEnabled, PsfLocationGroupPolicy, PsfLocationRegistry, PsfNone, PsfUseClientId, certenroll/ICertPropertyEnrollmentPolicyServer::GetUrlFlags, security.icertpropertyenrollmentpolicyserver_geturlflags
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
 - ICertPropertyEnrollmentPolicyServer::GetUrlFlags
 - certenroll/ICertPropertyEnrollmentPolicyServer::GetUrlFlags
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
 - ICertPropertyEnrollmentPolicyServer.GetUrlFlags
---

# ICertPropertyEnrollmentPolicyServer::GetUrlFlags


## -description

The <b>GetUrlFlags</b> method retrieves a set of flags that contain miscellaneous policy information about the certificate enrollment policy (CEP) server. These flags are set by the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertyenrollmentpolicyserver-initialize">Initialize</a> method.

## -parameters

### -param pValue [out, retval]

Pointer to a <a href="/windows/desktop/api/certenroll/ne-certenroll-policyserverurlflags">PolicyServerUrlFlags</a> enumeration value that specifies the  policy server flags. This can be a bitwise <b>OR</b> of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PsfNone"></a><a id="psfnone"></a><a id="PSFNONE"></a><dl>
<dt><b>PsfNone</b></dt>
</dl>
</td>
<td width="60%">
No flags are specified.

</td>
</tr>
<tr>
<td width="40%"><a id="PsfLocationGroupPolicy"></a><a id="psflocationgrouppolicy"></a><a id="PSFLOCATIONGROUPPOLICY"></a><dl>
<dt><b>PsfLocationGroupPolicy</b></dt>
</dl>
</td>
<td width="60%">
The policy server URL is specified in group policy by an administrator.

</td>
</tr>
<tr>
<td width="40%"><a id="PsfLocationRegistry"></a><a id="psflocationregistry"></a><a id="PSFLOCATIONREGISTRY"></a><dl>
<dt><b>PsfLocationRegistry</b></dt>
</dl>
</td>
<td width="60%">
The policy server URL is specified in the registry.

</td>
</tr>
<tr>
<td width="40%"><a id="PsfUseClientId"></a><a id="psfuseclientid"></a><a id="PSFUSECLIENTID"></a><dl>
<dt><b>PsfUseClientId</b></dt>
</dl>
</td>
<td width="60%">
Specifies that certificate enrollments and renewals include client specific data. Examples include the name of the cryptographic service provider, the Windows version number, the user name, the computer DNS name, and the domain controller DNS name. This flag is set when it is defined in group policy and is the default policy ID.

</td>
</tr>
<tr>
<td width="40%"><a id="PsfAutoEnrollmentEnabled"></a><a id="psfautoenrollmentenabled"></a><a id="PSFAUTOENROLLMENTENABLED"></a><dl>
<dt><b>PsfAutoEnrollmentEnabled</b></dt>
</dl>
</td>
<td width="60%">
Automatic certificate enrollment is enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="PsfAllowUnTrustedCA"></a><a id="psfallowuntrustedca"></a><a id="PSFALLOWUNTRUSTEDCA"></a><dl>
<dt><b>PsfAllowUnTrustedCA</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the certificate of the issuing CA need not be trusted by the client to install a certificate signed by the CA.

</td>
</tr>
</table>

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The <i>pValue</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyenrollmentpolicyserver">ICertPropertyEnrollmentPolicyServer</a>