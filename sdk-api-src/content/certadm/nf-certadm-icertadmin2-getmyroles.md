---
UID: NF:certadm.ICertAdmin2.GetMyRoles
title: ICertAdmin2::GetMyRoles (certadm.h)
description: Retrieves the certification authority (CA) roles of the caller.
helpviewer_keywords: ["CA_ACCESS_ADMIN","CA_ACCESS_AUDITOR","CA_ACCESS_ENROLL","CA_ACCESS_OFFICER","CA_ACCESS_OPERATOR","CA_ACCESS_READ","GetMyRoles","GetMyRoles method [Security]","GetMyRoles method [Security]","ICertAdmin2 interface","ICertAdmin2 interface [Security]","GetMyRoles method","ICertAdmin2.GetMyRoles","ICertAdmin2::GetMyRoles","certadm/ICertAdmin2::GetMyRoles","security.icertadmin2_getmyroles"]
old-location: security\icertadmin2_getmyroles.htm
tech.root: security
ms.assetid: 1378f1ad-1e01-4f09-869c-f450b9b2f454
ms.date: 12/05/2018
ms.keywords: CA_ACCESS_ADMIN, CA_ACCESS_AUDITOR, CA_ACCESS_ENROLL, CA_ACCESS_OFFICER, CA_ACCESS_OPERATOR, CA_ACCESS_READ, GetMyRoles, GetMyRoles method [Security], GetMyRoles method [Security],ICertAdmin2 interface, ICertAdmin2 interface [Security],GetMyRoles method, ICertAdmin2.GetMyRoles, ICertAdmin2::GetMyRoles, certadm/ICertAdmin2::GetMyRoles, security.icertadmin2_getmyroles
req.header: certadm.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Certidl.lib
req.dll: Certadm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertAdmin2::GetMyRoles
 - certadm/ICertAdmin2::GetMyRoles
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
 - ICertAdmin2.GetMyRoles
---

# ICertAdmin2::GetMyRoles


## -description

The <b>GetMyRoles</b> method retrieves the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) roles of the caller.

## -parameters

### -param strConfig [in]

String value that represents a valid configuration string for the CA in the form COMPUTERNAME\CANAME, where COMPUTERNAME is the Certificate Services server's network name, and CANAME is the common name of the CA, as entered during Certificate Services setup. For information about the configuration string name, see 
<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>.

<div class="alert"><b>Important</b>  <b>GetMyRoles</b> does not clear the internal cache when the configuration string is changed. When you change the configuration string for the CA, you must instantiate a new <a href="/windows/desktop/api/certadm/nn-certadm-icertadmin2">ICertAdmin</a> object and call this method again with the new configuration string.</div>
<div> </div>

### -param pRoles [out]

A pointer to a <b>LONG</b> value that represents the retrieved CA roles for the caller. This can be a bitwise combination of zero or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CA_ACCESS_ADMIN"></a><a id="ca_access_admin"></a><dl>
<dt><b>CA_ACCESS_ADMIN</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
Caller has CA administrator capability.

</td>
</tr>
<tr>
<td width="40%"><a id="CA_ACCESS_AUDITOR"></a><a id="ca_access_auditor"></a><dl>
<dt><b>CA_ACCESS_AUDITOR</b></dt>
<dt>0x4</dt>
</dl>
</td>
<td width="60%">
Caller has CA auditor capability.

</td>
</tr>
<tr>
<td width="40%"><a id="CA_ACCESS_ENROLL"></a><a id="ca_access_enroll"></a><dl>
<dt><b>CA_ACCESS_ENROLL</b></dt>
<dt>0x200</dt>
</dl>
</td>
<td width="60%">
Caller has enrollment access.

</td>
</tr>
<tr>
<td width="40%"><a id="CA_ACCESS_OFFICER"></a><a id="ca_access_officer"></a><dl>
<dt><b>CA_ACCESS_OFFICER</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
Caller has CA officer capability.

</td>
</tr>
<tr>
<td width="40%"><a id="CA_ACCESS_OPERATOR"></a><a id="ca_access_operator"></a><dl>
<dt><b>CA_ACCESS_OPERATOR</b></dt>
<dt>0x8</dt>
</dl>
</td>
<td width="60%">
Caller has CA backup capability.

</td>
</tr>
<tr>
<td width="40%"><a id="CA_ACCESS_READ"></a><a id="ca_access_read"></a><dl>
<dt><b>CA_ACCESS_READ</b></dt>
<dt>0x100</dt>
</dl>
</td>
<td width="60%">
Caller has CA read access.

</td>
</tr>
</table>

## -returns

<h3>C++</h3>
If the function is successful, the return value is S_OK.

 
If the function fails, the return value is an <b>HRESULT</b> that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
The return value is a <b>Long</b> value that represents the retrieved CA roles for the caller. This can be a bitwise combination of zero or more of the following values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CA_ACCESS_ADMIN</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
Caller has CA administrator capability.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CA_ACCESS_AUDITOR</b></dt>
<dt>0x4</dt>
</dl>
</td>
<td width="60%">
Caller has CA auditor capability.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CA_ACCESS_ENROLL</b></dt>
<dt>0x200</dt>
</dl>
</td>
<td width="60%">
Caller has enrollment access.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CA_ACCESS_OFFICER</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
Caller has CA officer capability.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CA_ACCESS_OPERATOR</b></dt>
<dt>0x8</dt>
</dl>
</td>
<td width="60%">
Caller has CA backup capability.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CA_ACCESS_READ</b></dt>
<dt>0x100</dt>
</dl>
</td>
<td width="60%">
Caller has read access.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/certadm/nn-certadm-icertadmin2">ICertAdmin2</a>