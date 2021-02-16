---
UID: NF:certadm.IOCSPAdmin.GetMyRoles
title: IOCSPAdmin::GetMyRoles (certadm.h)
description: Gets the access mask of privilege roles for a user on a given Online Certificate Status Protocol (OCSP) responder server.
helpviewer_keywords: ["GetMyRoles","GetMyRoles method [Security]","GetMyRoles method [Security]","IOCSPAdmin interface","IOCSPAdmin interface [Security]","GetMyRoles method","IOCSPAdmin.GetMyRoles","IOCSPAdmin::GetMyRoles","certadm/IOCSPAdmin::GetMyRoles","security.iocspadmin_getmyroles_method"]
old-location: security\iocspadmin_getmyroles_method.htm
tech.root: security
ms.assetid: b5a35e95-ec40-4154-8db9-fe5cd41960cb
ms.date: 12/05/2018
ms.keywords: GetMyRoles, GetMyRoles method [Security], GetMyRoles method [Security],IOCSPAdmin interface, IOCSPAdmin interface [Security],GetMyRoles method, IOCSPAdmin.GetMyRoles, IOCSPAdmin::GetMyRoles, certadm/IOCSPAdmin::GetMyRoles, security.iocspadmin_getmyroles_method
req.header: certadm.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certadm.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Certadm.lib
req.dll: Certadm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOCSPAdmin::GetMyRoles
 - certadm/IOCSPAdmin::GetMyRoles
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - IOCSPAdmin.GetMyRoles
---

# IOCSPAdmin::GetMyRoles


## -description

The <b>GetMyRoles</b> method gets the access mask of privilege roles for a user on a given Online Certificate Status Protocol (OCSP) responder server.

## -parameters

### -param bstrServerName [in]

A string that contains the responder-server name.

### -param pRoles [out]

A pointer to the 32-bit access mask.

## -returns

<h3>C++</h3>
 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
The 32-bit access mask.

## -remarks

The OCSP responder server defines the following masks for access privilege roles.

<table>
<tr>
<th>Constant</th>
<th>C++ value</th>
<th>VB Script value</th>
<th>Description</th>
</tr>
<tr>
<td>
CA_ACCESS_ADMIN

</td>
<td>
0x001

</td>
<td>
&amp;H1

</td>
<td>
CA administrator

</td>
</tr>
<tr>
<td>
CA_ACCESS_READ

</td>
<td>
0x100

</td>
<td>
&amp;H100

</td>
<td>
Read-only access to a CA

</td>
</tr>
<tr>
<td>
CA_ACCESS_ENROLL

</td>
<td>
0x200

</td>
<td>
&amp;H200

</td>
<td>
Enroll access to a CA

</td>
</tr>
</table>
 

Examples of privileges a user might have, depending on the  mask:

<ul>
<li>Configure and upgrade an OCSP server.</li>
<li>Assign existing signing certificate and key.</li>
<li>Install and update Certificate Revocation Lists (CRLs).</li>
<li>Configure a  response format.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certadm/nn-certadm-iocspadmin">IOCSPAdmin</a>