---
UID: NS:ntsecapi._KERB_CERTIFICATE_LOGON
title: KERB_CERTIFICATE_LOGON (ntsecapi.h)
description: Contains information about a smart card logon session. (KERB_CERTIFICATE_LOGON)
helpviewer_keywords: ["*PKERB_CERTIFICATE_LOGON","KERB_CERTIFICATE_LOGON","KERB_CERTIFICATE_LOGON structure [Security]","KERB_CERTIFICATE_LOGON_FLAG_CHECK_DUPLICATES","KERB_CERTIFICATE_LOGON_FLAG_USE_CERTIFICATE_INFO","KerbCertificateLogon","KerbCertificateUnlockLogon","PKERB_CERTIFICATE_LOGON","PKERB_CERTIFICATE_LOGON structure pointer [Security]","ntsecapi/KERB_CERTIFICATE_LOGON","ntsecapi/PKERB_CERTIFICATE_LOGON","security.kerb_certificate_logon"]
old-location: security\kerb_certificate_logon.htm
tech.root: security
ms.assetid: e6aa0042-edb5-4e9b-b545-5159d3bfb8fc
ms.date: 12/05/2018
ms.keywords: '*PKERB_CERTIFICATE_LOGON, KERB_CERTIFICATE_LOGON, KERB_CERTIFICATE_LOGON structure [Security], KERB_CERTIFICATE_LOGON_FLAG_CHECK_DUPLICATES, KERB_CERTIFICATE_LOGON_FLAG_USE_CERTIFICATE_INFO, KerbCertificateLogon, KerbCertificateUnlockLogon, PKERB_CERTIFICATE_LOGON, PKERB_CERTIFICATE_LOGON structure pointer [Security], ntsecapi/KERB_CERTIFICATE_LOGON, ntsecapi/PKERB_CERTIFICATE_LOGON, security.kerb_certificate_logon'
req.header: ntsecapi.h
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: KERB_CERTIFICATE_LOGON, *PKERB_CERTIFICATE_LOGON
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _KERB_CERTIFICATE_LOGON
 - ntsecapi/_KERB_CERTIFICATE_LOGON
 - PKERB_CERTIFICATE_LOGON
 - ntsecapi/PKERB_CERTIFICATE_LOGON
 - KERB_CERTIFICATE_LOGON
 - ntsecapi/KERB_CERTIFICATE_LOGON
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - KERB_CERTIFICATE_LOGON
---

# KERB_CERTIFICATE_LOGON structure


## -description

The <b>KERB_CERTIFICATE_LOGON</b> structure contains information about a smart card <a href="/windows/desktop/SecGloss/l-gly">logon session</a>.

It is passed as the <i>AuthenticationInformation</i> parameter to the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser">LsaLogonUser</a> function when the <a href="/windows/desktop/SecAuthN/kerberos-ssp-ap">Kerberos</a> security package performs an interactive smart card logon.

## -struct-fields

### -field MessageType

A member of the <a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-kerb_logon_submit_type">KERB_LOGON_SUBMIT_TYPE</a> enumeration that indicates how this structure is used. The member must be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="KerbCertificateLogon"></a><a id="kerbcertificatelogon"></a><a id="KERBCERTIFICATELOGON"></a><dl>
<dt><b>KerbCertificateLogon</b></dt>
<dt>13</dt>
</dl>
</td>
<td width="60%">
This structure is passed as the <i>AuthenticationInformation</i> parameter to the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser">LsaLogonUser</a> function to perform an interactive smart card logon.

</td>
</tr>
<tr>
<td width="40%"><a id="KerbCertificateUnlockLogon"></a><a id="kerbcertificateunlocklogon"></a><a id="KERBCERTIFICATEUNLOCKLOGON"></a><dl>
<dt><b>KerbCertificateUnlockLogon</b></dt>
<dt>15</dt>
</dl>
</td>
<td width="60%">
This structure is used as the <b>Logon</b> member of a <a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-kerb_certificate_unlock_logon">KERB_CERTIFICATE_UNLOCK_LOGON</a> structure.

</td>
</tr>
</table>

### -field DomainName

The domain name of the user to authenticate. The value of this member can be empty. If the value is not empty, <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser">LsaLogonUser</a> uses the value to locate the <a href="/windows/desktop/SecGloss/k-gly">Key Distribution Center</a> (KDC). If the value is empty, <b>LsaLogonUser</b> attempts to authenticate against the domain to which the computer is joined.  The pointer is relative to the beginning of the structure and is not an absolute memory pointer.

### -field UserName

The user name of the user to authenticate. The value of this member can be empty. If the value is not empty, <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser">LsaLogonUser</a> uses the value to locate the user account to authenticate.  The pointer is relative to the beginning of the structure and is not an absolute memory pointer.

### -field Pin

The PIN to use to authenticate the user. The <b>Length</b> member of this structure does not include the terminating null character of the PIN. The pointer is relative to the beginning of the structure and is not an absolute memory pointer.

The PIN can be protected by using the <a href="/windows/desktop/api/wincred/nf-wincred-credprotecta">CredProtect</a> function.

### -field Flags

Optional flags that control the behavior of the authentication. The following values are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="KERB_CERTIFICATE_LOGON_FLAG_CHECK_DUPLICATES"></a><a id="kerb_certificate_logon_flag_check_duplicates"></a><dl>
<dt><b>KERB_CERTIFICATE_LOGON_FLAG_CHECK_DUPLICATES</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
The KDC checks the certificate for multiple account mappings.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_CERTIFICATE_LOGON_FLAG_USE_CERTIFICATE_INFO"></a><a id="kerb_certificate_logon_flag_use_certificate_info"></a><dl>
<dt><b>KERB_CERTIFICATE_LOGON_FLAG_USE_CERTIFICATE_INFO</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
The KDC uses the certificate information for authentication.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:  </b>This flag is not available.

</td>
</tr>
</table>

### -field CspDataLength

The length, in characters, of the <b>CspData</b> member.

### -field CspData

A pointer to a <a href="/windows/desktop/SecAuthN/kerb-smartcard-csp-info">KERB_SMARTCARD_CSP_INFO</a> structure that contains information about the smart card <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) ) or a pointer to a marshaled <a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-kerb_certificate_info">KERB_CERTIFICATE_INFO</a> structure when updating certificate credentials.

## -remarks

This structure, along with the data pointed to by the <b>DomainName</b>, <b>UserName</b>, <b>Pin</b>, and <b>CspData</b> members, is contained in a single block of contiguous memory. When this structure is serialized, the offsets specified by each of these members must be multiples of two.

The pointers stored in the members of <b>UNICODE_STRING</b> type are relative to the beginning of the structure and are not absolute memory pointers.

## -see-also

<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-kerb_certificate_unlock_logon">KERB_CERTIFICATE_UNLOCK_LOGON</a>



<a href="/windows/desktop/SecAuthN/kerb-smartcard-csp-info">KERB_SMARTCARD_CSP_INFO</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser">LsaLogonUser</a>
