---
UID: NF:certenroll.IX509EnrollmentPolicyServer.GetUseClientId
title: IX509EnrollmentPolicyServer::GetUseClientId (certenroll.h)
description: Retrieves a value that specifies whether the ClientId attribute is set in the policy server flags of the certificate enrollment policy (CEP) server.
helpviewer_keywords: ["GetUseClientId","GetUseClientId method [Security]","GetUseClientId method [Security]","IX509EnrollmentPolicyServer interface","IX509EnrollmentPolicyServer interface [Security]","GetUseClientId method","IX509EnrollmentPolicyServer.GetUseClientId","IX509EnrollmentPolicyServer::GetUseClientId","certenroll/IX509EnrollmentPolicyServer::GetUseClientId","security.ix509enrollmentpolicyserver_getuseclientid"]
old-location: security\ix509enrollmentpolicyserver_getuseclientid.htm
tech.root: security
ms.assetid: 5fd74752-60bb-4bdb-973d-76d4ab0ae4c4
ms.date: 12/05/2018
ms.keywords: GetUseClientId, GetUseClientId method [Security], GetUseClientId method [Security],IX509EnrollmentPolicyServer interface, IX509EnrollmentPolicyServer interface [Security],GetUseClientId method, IX509EnrollmentPolicyServer.GetUseClientId, IX509EnrollmentPolicyServer::GetUseClientId, certenroll/IX509EnrollmentPolicyServer::GetUseClientId, security.ix509enrollmentpolicyserver_getuseclientid
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
 - IX509EnrollmentPolicyServer::GetUseClientId
 - certenroll/IX509EnrollmentPolicyServer::GetUseClientId
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
 - IX509EnrollmentPolicyServer.GetUseClientId
---

# IX509EnrollmentPolicyServer::GetUseClientId


## -description

The <b>GetUseClientId</b> method retrieves a value that specifies whether the <b>ClientId</b> attribute is set in the policy server flags of the certificate enrollment policy (CEP) server.

## -parameters

### -param pValue [out, retval]

Pointer to a Boolean value that specifies whether the <b>PsfUseClientId</b> bit is set on the <a href="/windows/desktop/api/certenroll/ne-certenroll-policyserverurlflags">PolicyServerUrlFlags</a> enumeration for this certificate enrollment policy (CEP) server.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pValue</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This method returns <b>VARIANT_TRUE</b> if the <b>PsfUseClientId</b> bit is set on the <a href="/windows/desktop/api/certenroll/ne-certenroll-policyserverurlflags">PolicyServerUrlFlags</a> enumeration for this CEP server. If this flag is set, the <b>ClientID</b> attribute is included in certificate requests during the enrollment process and can be used by the certification authority for diagnostic or auditing purposes. Examples of the type of information included in this attribute include the name of the cryptographic service provider, the Windows version number, the user name, the computer DNS name, and the domain controller DNS name.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmentpolicyserver">IX509EnrollmentPolicyServer</a>