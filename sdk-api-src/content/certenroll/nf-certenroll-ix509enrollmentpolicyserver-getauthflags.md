---
UID: NF:certenroll.IX509EnrollmentPolicyServer.GetAuthFlags
title: IX509EnrollmentPolicyServer::GetAuthFlags (certenroll.h)
description: Retrieves a value that specifies the authentication type used by the client to authenticate itself to the certificate enrollment policy (CEP) server.
helpviewer_keywords: ["GetAuthFlags","GetAuthFlags method [Security]","GetAuthFlags method [Security]","IX509EnrollmentPolicyServer interface","IX509EnrollmentPolicyServer interface [Security]","GetAuthFlags method","IX509EnrollmentPolicyServer.GetAuthFlags","IX509EnrollmentPolicyServer::GetAuthFlags","X509AuthAnonymous","X509AuthCertificate","X509AuthKerberos","X509AuthUsername","certenroll/IX509EnrollmentPolicyServer::GetAuthFlags","security.ix509enrollmentpolicyserver_getauthflags"]
old-location: security\ix509enrollmentpolicyserver_getauthflags.htm
tech.root: security
ms.assetid: 29ecfb93-82ec-4d34-84ea-0a181e134b6a
ms.date: 12/05/2018
ms.keywords: GetAuthFlags, GetAuthFlags method [Security], GetAuthFlags method [Security],IX509EnrollmentPolicyServer interface, IX509EnrollmentPolicyServer interface [Security],GetAuthFlags method, IX509EnrollmentPolicyServer.GetAuthFlags, IX509EnrollmentPolicyServer::GetAuthFlags, X509AuthAnonymous, X509AuthCertificate, X509AuthKerberos, X509AuthUsername, certenroll/IX509EnrollmentPolicyServer::GetAuthFlags, security.ix509enrollmentpolicyserver_getauthflags
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
 - IX509EnrollmentPolicyServer::GetAuthFlags
 - certenroll/IX509EnrollmentPolicyServer::GetAuthFlags
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
 - IX509EnrollmentPolicyServer.GetAuthFlags
---

# IX509EnrollmentPolicyServer::GetAuthFlags


## -description

The <b>GetAuthFlags</b> method retrieves a value that specifies the authentication type used by the client to authenticate itself to the certificate enrollment policy (CEP) server. This value is set by the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertyenrollmentpolicyserver-initialize">Initialize</a> method on the <a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyenrollmentpolicyserver">ICertPropertyEnrollmentPolicyServer</a> interface.

## -parameters

### -param pValue [out, retval]

Pointer to an <a href="/windows/desktop/api/certcli/ne-certcli-x509enrollmentauthflags">X509EnrollmentAuthFlags</a>  enumeration value that specifies the authentication type. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="X509AuthAnonymous"></a><a id="x509authanonymous"></a><a id="X509AUTHANONYMOUS"></a><dl>
<dt><b>X509AuthAnonymous</b></dt>
</dl>
</td>
<td width="60%">
Anonymous authentication.

</td>
</tr>
<tr>
<td width="40%"><a id="X509AuthKerberos"></a><a id="x509authkerberos"></a><a id="X509AUTHKERBEROS"></a><dl>
<dt><b>X509AuthKerberos</b></dt>
</dl>
</td>
<td width="60%">
Kerberos authentication.

</td>
</tr>
<tr>
<td width="40%"><a id="X509AuthUsername"></a><a id="x509authusername"></a><a id="X509AUTHUSERNAME"></a><dl>
<dt><b>X509AuthUsername</b></dt>
</dl>
</td>
<td width="60%">
Clear text user name and password authentication.

</td>
</tr>
<tr>
<td width="40%"><a id="X509AuthCertificate"></a><a id="x509authcertificate"></a><a id="X509AUTHCERTIFICATE"></a><dl>
<dt><b>X509AuthCertificate</b></dt>
</dl>
</td>
<td width="60%">
Client authentication certificate installed on the local computer and used by the server to verify the identity of the client.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pValue</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmentpolicyserver">IX509EnrollmentPolicyServer</a>