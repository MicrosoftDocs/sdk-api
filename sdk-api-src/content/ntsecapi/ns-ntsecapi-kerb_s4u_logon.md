---
UID: NS:ntsecapi._KERB_S4U_LOGON
title: KERB_S4U_LOGON (ntsecapi.h)
description: Contains information about a service for user (S4U) logon.
helpviewer_keywords: ["*PKERB_S4U_LOGON","KERB_S4U_LOGON","KERB_S4U_LOGON structure [Security]","KERB_S4U_LOGON_FLAG_CHECK_LOGONHOURS","KERB_S4U_LOGON_FLAG_IDENTITY","PKERB_S4U_LOGON","PKERB_S4U_LOGON structure pointer [Security]","ntsecapi/KERB_S4U_LOGON","ntsecapi/PKERB_S4U_LOGON","security.kerb_s4u_logon"]
old-location: security\kerb_s4u_logon.htm
tech.root: security
ms.assetid: ab94c36b-7aba-452d-abc0-220c91ffacca
ms.date: 12/05/2018
ms.keywords: '*PKERB_S4U_LOGON, KERB_S4U_LOGON, KERB_S4U_LOGON structure [Security], KERB_S4U_LOGON_FLAG_CHECK_LOGONHOURS, KERB_S4U_LOGON_FLAG_IDENTITY, PKERB_S4U_LOGON, PKERB_S4U_LOGON structure pointer [Security], ntsecapi/KERB_S4U_LOGON, ntsecapi/PKERB_S4U_LOGON, security.kerb_s4u_logon'
req.header: ntsecapi.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: KERB_S4U_LOGON, *PKERB_S4U_LOGON
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _KERB_S4U_LOGON
 - ntsecapi/_KERB_S4U_LOGON
 - PKERB_S4U_LOGON
 - ntsecapi/PKERB_S4U_LOGON
 - KERB_S4U_LOGON
 - ntsecapi/KERB_S4U_LOGON
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
 - KERB_S4U_LOGON
---

# KERB_S4U_LOGON structure


## -description

The <b>KERB_S4U_LOGON</b> structure contains information about a service for user (S4U) logon. This structure is used by the <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser">LsaLogonUser</a> function with the <a href="/windows/desktop/SecGloss/k-gly">Kerberos</a> package.

## -struct-fields

### -field MessageType

A value of the <a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-kerb_logon_submit_type">KERB_LOGON_SUBMIT_TYPE</a> enumeration that identifies the type of logon being requested. This member must be set to <b>KerbS4ULogon</b>.

### -field Flags

Flags that provide more information about the logon.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="KERB_S4U_LOGON_FLAG_CHECK_LOGONHOURS"></a><a id="kerb_s4u_logon_flag_check_logonhours"></a><dl>
<dt><b>KERB_S4U_LOGON_FLAG_CHECK_LOGONHOURS</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
Requests the hours that the user has been logged on.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_S4U_LOGON_FLAG_IDENTIFY"></a><a id="kerb_s4u_logon_flag_identify"></a><dl>
<dt><b>KERB_S4U_LOGON_FLAG_IDENTIFY</b></dt>
<dt>0x8</dt>
</dl>
</td>
<td width="60%">
Requests the identity token.

</td>
</tr>
</table>

### -field ClientUpn

A <a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> that specifies the <a href="/windows/desktop/SecGloss/u-gly">user principal name</a> (UPN) of the client. This member cannot be <b>NULL</b>.

The <b>Buffer</b> member of the <a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> structure must point to memory that is contiguous to the <b>KERB_S4U_LOGON</b> structure.

### -field ClientRealm

A <a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> that specifies the realm of the client, if known. If the realm is not known, this member can be <b>NULL</b>.

The <b>Buffer</b> member of the <a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> structure must point to memory that is contiguous to the <b>KERB_S4U_LOGON</b> structure.