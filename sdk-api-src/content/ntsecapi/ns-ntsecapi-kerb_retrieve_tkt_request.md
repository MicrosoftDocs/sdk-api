---
UID: NS:ntsecapi._KERB_RETRIEVE_TKT_REQUEST
title: KERB_RETRIEVE_TKT_REQUEST (ntsecapi.h)
description: Contains information used to retrieve a ticket.
helpviewer_keywords: ["*PKERB_RETRIEVE_TKT_REQUEST",">127","KERB_ETYPE_DES_CBC_CRC","KERB_ETYPE_DES_CBC_MD4","KERB_ETYPE_DES_CBC_MD5","KERB_ETYPE_NULL","KERB_ETYPE_RC4_HMAC_NT","KERB_ETYPE_RC4_MD4","KERB_RETRIEVE_TICKET_AS_KERB_CRED","KERB_RETRIEVE_TICKET_CACHE_TICKET","KERB_RETRIEVE_TICKET_DONT_USE_CACHE","KERB_RETRIEVE_TICKET_MAX_LIFETIME","KERB_RETRIEVE_TICKET_USE_CACHE_ONLY","KERB_RETRIEVE_TICKET_USE_CREDHANDLE","KERB_RETRIEVE_TICKET_WITH_SEC_CRED","KERB_RETRIEVE_TKT_REQUEST","KERB_RETRIEVE_TKT_REQUEST structure [Security]","PKERB_RETRIEVE_TKT_REQUEST","PKERB_RETRIEVE_TKT_REQUEST structure pointer [Security]","_lsa_kerb_retrieve_tkt_request","ntsecapi/KERB_RETRIEVE_TKT_REQUEST","ntsecapi/PKERB_RETRIEVE_TKT_REQUEST","security.kerb_retrieve_tkt_request"]
old-location: security\kerb_retrieve_tkt_request.htm
tech.root: security
ms.assetid: 3b088c94-810b-44c7-887a-58e8dbd13603
ms.date: 12/05/2018
ms.keywords: '*PKERB_RETRIEVE_TKT_REQUEST, >127, KERB_ETYPE_DES_CBC_CRC, KERB_ETYPE_DES_CBC_MD4, KERB_ETYPE_DES_CBC_MD5, KERB_ETYPE_NULL, KERB_ETYPE_RC4_HMAC_NT, KERB_ETYPE_RC4_MD4, KERB_RETRIEVE_TICKET_AS_KERB_CRED, KERB_RETRIEVE_TICKET_CACHE_TICKET, KERB_RETRIEVE_TICKET_DONT_USE_CACHE, KERB_RETRIEVE_TICKET_MAX_LIFETIME, KERB_RETRIEVE_TICKET_USE_CACHE_ONLY, KERB_RETRIEVE_TICKET_USE_CREDHANDLE, KERB_RETRIEVE_TICKET_WITH_SEC_CRED, KERB_RETRIEVE_TKT_REQUEST, KERB_RETRIEVE_TKT_REQUEST structure [Security], PKERB_RETRIEVE_TKT_REQUEST, PKERB_RETRIEVE_TKT_REQUEST structure pointer [Security], _lsa_kerb_retrieve_tkt_request, ntsecapi/KERB_RETRIEVE_TKT_REQUEST, ntsecapi/PKERB_RETRIEVE_TKT_REQUEST, security.kerb_retrieve_tkt_request'
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: KERB_RETRIEVE_TKT_REQUEST, *PKERB_RETRIEVE_TKT_REQUEST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _KERB_RETRIEVE_TKT_REQUEST
 - ntsecapi/_KERB_RETRIEVE_TKT_REQUEST
 - PKERB_RETRIEVE_TKT_REQUEST
 - ntsecapi/PKERB_RETRIEVE_TKT_REQUEST
 - KERB_RETRIEVE_TKT_REQUEST
 - ntsecapi/KERB_RETRIEVE_TKT_REQUEST
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
 - KERB_RETRIEVE_TKT_REQUEST
---

# KERB_RETRIEVE_TKT_REQUEST structure


## -description

The <b>KERB_RETRIEVE_TKT_REQUEST</b> structure contains information used to retrieve a ticket.

It is used by 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a>.The Kerberos ticket is defined in Internet <a href="http://www.ietf.org/rfc/rfc4120.txt">RFC 4120</a>. For more information, see <a href="https://www.ietf.org/">http://www.ietf.org</a>.

## -struct-fields

### -field MessageType

<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-kerb_protocol_message_type">KERB_PROTOCOL_MESSAGE_TYPE</a> value indicating the type of request being made. This member must be set to <b>KerbRetrieveEncodedTicketMessage</b>.

### -field LogonId

<a href="/windows/desktop/api/winnt/ns-winnt-luid">LUID</a> structure containing the <a href="/windows/desktop/SecGloss/l-gly">logon session</a> identifier. This can be zero for the current user's logon session. If not zero, the caller must have the SeTcbPrivilege privilege set. If this fails, the <a href="/windows/desktop/SecGloss/k-gly">Kerberos</a> authentication package sets the <i>ProtocolStatus</i> parameter of <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a> to STATUS_ACCESS_DENIED.

### -field TargetName

<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> containing the name of the target service.

### -field TicketFlags

Contains flags specifying uses for the retrieved ticket. If <b>TicketFlags</b> is set to zero and if there is a matching ticket found in the cache, then that ticket will be returned, regardless of its flag values. If there is no match in the cache, a new ticket with the default flag values will be requested. 




If this member is not set to zero, the returned ticket will not be cached.

### -field CacheOptions

Indicates options for searching the cache. Set this member to zero to indicate that the cache should be searched and if no ticket if found, a new ticket should be requested. 




If this member is not set to zero, the returned ticket will not be cached.

<b>CacheOptions</b> can contain the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="KERB_RETRIEVE_TICKET_DONT_USE_CACHE"></a><a id="kerb_retrieve_ticket_dont_use_cache"></a><dl>
<dt><b>KERB_RETRIEVE_TICKET_DONT_USE_CACHE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Always request a new ticket; do not search the cache. 




If a ticket is obtained, the Kerberos authentication package returns STATUS_SUCCESS in the <i>ProtocolStatus</i> parameter of the <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_RETRIEVE_TICKET_USE_CREDHANDLE"></a><a id="kerb_retrieve_ticket_use_credhandle"></a><dl>
<dt><b>KERB_RETRIEVE_TICKET_USE_CREDHANDLE</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Use the <b>CredentialsHandle</b> member instead of <b>LogonId</b> to identify the logon session. The credential handle is used as the client credential for which the ticket is retrieved

<b>Note</b>  This option is not available for 32-bit Windows-based applications running on 64-bit Windows.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_RETRIEVE_TICKET_USE_CACHE_ONLY"></a><a id="kerb_retrieve_ticket_use_cache_only"></a><dl>
<dt><b>KERB_RETRIEVE_TICKET_USE_CACHE_ONLY</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Return only a previously cached ticket. 




If such a ticket is not found, the Kerberos authentication package returns STATUS_OBJECT_NAME_NOT_FOUND in the <i>ProtocolStatus</i> parameter of the <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_RETRIEVE_TICKET_AS_KERB_CRED"></a><a id="kerb_retrieve_ticket_as_kerb_cred"></a><dl>
<dt><b>KERB_RETRIEVE_TICKET_AS_KERB_CRED</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
Return the ticket as a Kerberos credential. The Kerberos ticket is defined in Internet <a href="http://www.ietf.org/rfc/rfc4120.txt">RFC 4120</a> as KRB_CRED. For more information, see <a href="https://www.ietf.org/">http://www.ietf.org</a>. 



							

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_RETRIEVE_TICKET_WITH_SEC_CRED"></a><a id="kerb_retrieve_ticket_with_sec_cred"></a><dl>
<dt><b>KERB_RETRIEVE_TICKET_WITH_SEC_CRED</b></dt>
<dt>10</dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_RETRIEVE_TICKET_CACHE_TICKET"></a><a id="kerb_retrieve_ticket_cache_ticket"></a><dl>
<dt><b>KERB_RETRIEVE_TICKET_CACHE_TICKET</b></dt>
<dt>20</dt>
</dl>
</td>
<td width="60%">
Return the ticket that is currently in the cache. If the ticket is not in the cache, it is requested and then cached. This flag should not be used with the KERB_RETRIEVE_TICKET_DONT_USE_CACHE flag. 




<b>Windows XP with SP1 and earlier and Windows Server 2003:  </b>This option is not available.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_RETRIEVE_TICKET_MAX_LIFETIME"></a><a id="kerb_retrieve_ticket_max_lifetime"></a><dl>
<dt><b>KERB_RETRIEVE_TICKET_MAX_LIFETIME</b></dt>
<dt>40</dt>
</dl>
</td>
<td width="60%">
Return a fresh ticket with maximum allowed time by the policy. The ticker is cached afterwards. Use of this flag implies that KERB_RETRIEVE_TICKET_USE_CACHE_ONLY is not set and KERB_RETRIEVE_TICKET_CACHE_TICKET is set. 




<b>Windows Vista, Windows Server 2008, Windows XP with SP1 and earlier and Windows Server 2003:  </b>This option is not available.

</td>
</tr>
</table>

### -field EncryptionType

Specifies the type of encryption to use for the requested ticket. If this member is not set to zero, the returned ticket will not be cached. 




This member can have one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="KERB_ETYPE_DES_CBC_CRC"></a><a id="kerb_etype_des_cbc_crc"></a><dl>
<dt><b>KERB_ETYPE_DES_CBC_CRC</b></dt>
</dl>
</td>
<td width="60%">
Use <a href="/windows/desktop/SecGloss/d-gly">DES</a> encryption in <a href="/windows/desktop/SecGloss/c-gly">cipher-block-chaining</a> mode with a CRC-32 checksum.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_ETYPE_DES_CBC_MD4"></a><a id="kerb_etype_des_cbc_md4"></a><dl>
<dt><b>KERB_ETYPE_DES_CBC_MD4</b></dt>
</dl>
</td>
<td width="60%">
Use DES encryption in cipher-block-chaining mode with a MD4 checksum.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_ETYPE_DES_CBC_MD5"></a><a id="kerb_etype_des_cbc_md5"></a><dl>
<dt><b>KERB_ETYPE_DES_CBC_MD5</b></dt>
</dl>
</td>
<td width="60%">
Use DES encryption in cipher-block-chaining mode with a MD5 checksum.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_ETYPE_NULL"></a><a id="kerb_etype_null"></a><dl>
<dt><b>KERB_ETYPE_NULL</b></dt>
</dl>
</td>
<td width="60%">
Use no encryption.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_ETYPE_RC4_HMAC_NT"></a><a id="kerb_etype_rc4_hmac_nt"></a><dl>
<dt><b>KERB_ETYPE_RC4_HMAC_NT</b></dt>
</dl>
</td>
<td width="60%">
Use the RC4 <a href="/windows/desktop/SecGloss/s-gly">stream cipher</a> with a <a href="/windows/desktop/SecGloss/h-gly">hash</a>-based <a href="/windows/desktop/SecGloss/m-gly">Message Authentication Code</a> (MAC), as used by Windows.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_ETYPE_RC4_MD4"></a><a id="kerb_etype_rc4_md4"></a><dl>
<dt><b>KERB_ETYPE_RC4_MD4</b></dt>
</dl>
</td>
<td width="60%">
Use the RC4 stream cipher with the MD4 hash function.

</td>
</tr>
<tr>
<td width="40%"><a id="_127"></a><dl>
<dt><b>&gt;127</b></dt>
</dl>
</td>
<td width="60%">
Values greater than 127 are reserved for local values and may change without notice.

</td>
</tr>
</table>

### -field CredentialsHandle

An SSPI credentials handle used in place of a logon session identifier.