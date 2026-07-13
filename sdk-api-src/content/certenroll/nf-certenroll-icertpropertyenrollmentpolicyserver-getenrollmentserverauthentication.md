---
UID: NF:certenroll.ICertPropertyEnrollmentPolicyServer.GetEnrollmentServerAuthentication
title: ICertPropertyEnrollmentPolicyServer::GetEnrollmentServerAuthentication (certenroll.h)
description: The GetEnrollmentServerAuthentication method retrieves a value that specifies the type of authentication used by the certificate enrollment server (CES) to authenticate a client. This value is set by the Initialize method.
helpviewer_keywords: ["GetEnrollmentServerAuthentication","GetEnrollmentServerAuthentication method [Security]","GetEnrollmentServerAuthentication method [Security]","ICertPropertyEnrollmentPolicyServer interface","ICertPropertyEnrollmentPolicyServer interface [Security]","GetEnrollmentServerAuthentication method","ICertPropertyEnrollmentPolicyServer.GetEnrollmentServerAuthentication","ICertPropertyEnrollmentPolicyServer::GetEnrollmentServerAuthentication","X509AuthAnonymous","X509AuthCertificate","X509AuthKerberos","X509AuthUsername","certenroll/ICertPropertyEnrollmentPolicyServer::GetEnrollmentServerAuthentication","security.icertpropertyenrollmentpolicyserver_getenrollmentserverauthentication"]
old-location: security\icertpropertyenrollmentpolicyserver_getenrollmentserverauthentication.htm
tech.root: security
ms.assetid: c46d9bc4-26ee-40c0-a228-804e7c598285
ms.date: 12/05/2018
ms.keywords: GetEnrollmentServerAuthentication, GetEnrollmentServerAuthentication method [Security], GetEnrollmentServerAuthentication method [Security],ICertPropertyEnrollmentPolicyServer interface, ICertPropertyEnrollmentPolicyServer interface [Security],GetEnrollmentServerAuthentication method, ICertPropertyEnrollmentPolicyServer.GetEnrollmentServerAuthentication, ICertPropertyEnrollmentPolicyServer::GetEnrollmentServerAuthentication, X509AuthAnonymous, X509AuthCertificate, X509AuthKerberos, X509AuthUsername, certenroll/ICertPropertyEnrollmentPolicyServer::GetEnrollmentServerAuthentication, security.icertpropertyenrollmentpolicyserver_getenrollmentserverauthentication
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
 - ICertPropertyEnrollmentPolicyServer::GetEnrollmentServerAuthentication
 - certenroll/ICertPropertyEnrollmentPolicyServer::GetEnrollmentServerAuthentication
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
 - ICertPropertyEnrollmentPolicyServer.GetEnrollmentServerAuthentication
---

# ICertPropertyEnrollmentPolicyServer::GetEnrollmentServerAuthentication


## -description

The <b>GetEnrollmentServerAuthentication</b> method retrieves a value that specifies the type of authentication used by the certificate enrollment server (CES) to authenticate a client. This value is set by the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertyenrollmentpolicyserver-initialize">Initialize</a> method.

## -parameters

### -param pValue [out, retval]

An <a href="/windows/desktop/api/certcli/ne-certcli-x509enrollmentauthflags">X509EnrollmentAuthFlags</a> enumeration value that specifies the client authentication type. This can be one of the following values.

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

<div class="alert"><b>Note</b>  The user name and password are encrypted before transmission and are stored securely in the credential vault on the certificate enrollment server.</div>
<div> </div>
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