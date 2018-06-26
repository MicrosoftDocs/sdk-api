---
UID: NS:ntsecapi._KERB_EXTERNAL_NAME
title: "_KERB_EXTERNAL_NAME"
author: windows-sdk-content
description: Contains information about an external name.
old-location: security\kerb_external_name.htm
old-project: SecAuthN
ms.assetid: 8ed37546-6443-4010-a078-4359dd1c2861
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "*PKERB_EXTERNAL_NAME, KERB_EXTERNAL_NAME, KERB_EXTERNAL_NAME structure [Security], KRB_NT_ENTERPRISE_PRINCIPAL, KRB_NT_ENT_PRINCIPAL_AND_ID, KRB_NT_MS_PRINCIPAL_AND_ID, KRB_NT_MS_PRINICPAL, KRB_NT_PRINCIPAL, KRB_NT_SRV_HST, KRB_NT_SRV_INST, KRB_NT_SRV_XHST, KRB_NT_UID, KRB_NT_UNKNOWN, PKERB_EXTERNAL_NAME, PKERB_EXTERNAL_NAME structure pointer [Security], _KERB_EXTERNAL_NAME, _lsa_kerb_external_name, ntsecapi/KERB_EXTERNAL_NAME, ntsecapi/PKERB_EXTERNAL_NAME, security.kerb_external_name"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: KERB_EXTERNAL_NAME, *PKERB_EXTERNAL_NAME
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - KERB_EXTERNAL_NAME
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _KERB_EXTERNAL_NAME structure


## -description


The <b>KERB_EXTERNAL_NAME</b> structure contains information about an external name.

An external name is one used by external users. This structure is used by the 
<a href="https://msdn.microsoft.com/742e2795-ec74-4856-a680-7a1c233a2934">KERB_EXTERNAL_TICKET</a> structure.


## -struct-fields




### -field NameType

Indicates the type of the names stored in this structure.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="KRB_NT_UNKNOWN"></a><a id="krb_nt_unknown"></a><dl>
<dt><b>KRB_NT_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
Unknown name type.

</td>
</tr>
<tr>
<td width="40%"><a id="KRB_NT_PRINCIPAL"></a><a id="krb_nt_principal"></a><dl>
<dt><b>KRB_NT_PRINCIPAL</b></dt>
</dl>
</td>
<td width="60%">
Name of the user or a Kerberos name type principal in the case of a DCE.

</td>
</tr>
<tr>
<td width="40%"><a id="KRB_NT_SRV_INST"></a><a id="krb_nt_srv_inst"></a><dl>
<dt><b>KRB_NT_SRV_INST</b></dt>
</dl>
</td>
<td width="60%">
Service name and other unique name as instance (krbtgt).

</td>
</tr>
<tr>
<td width="40%"><a id="KRB_NT_SRV_HST"></a><a id="krb_nt_srv_hst"></a><dl>
<dt><b>KRB_NT_SRV_HST</b></dt>
</dl>
</td>
<td width="60%">
Service name with host name as instance (telnet, rcommands).

</td>
</tr>
<tr>
<td width="40%"><a id="KRB_NT_SRV_XHST"></a><a id="krb_nt_srv_xhst"></a><dl>
<dt><b>KRB_NT_SRV_XHST</b></dt>
</dl>
</td>
<td width="60%">
Service name with host as instance other than krbtgt, telnet, or rcommands.

</td>
</tr>
<tr>
<td width="40%"><a id="KRB_NT_UID"></a><a id="krb_nt_uid"></a><dl>
<dt><b>KRB_NT_UID</b></dt>
</dl>
</td>
<td width="60%">
Unique ID.

</td>
</tr>
<tr>
<td width="40%"><a id="KRB_NT_ENTERPRISE_PRINCIPAL"></a><a id="krb_nt_enterprise_principal"></a><dl>
<dt><b>KRB_NT_ENTERPRISE_PRINCIPAL</b></dt>
</dl>
</td>
<td width="60%">
User principal name (UPN) or <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">service principal name</a> (SPN).

</td>
</tr>
<tr>
<td width="40%"><a id="KRB_NT_ENT_PRINCIPAL_AND_ID"></a><a id="krb_nt_ent_principal_and_id"></a><dl>
<dt><b>KRB_NT_ENT_PRINCIPAL_AND_ID</b></dt>
</dl>
</td>
<td width="60%">
UPN and <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID).

</td>
</tr>
<tr>
<td width="40%"><a id="KRB_NT_MS_PRINICPAL"></a><a id="krb_nt_ms_prinicpal"></a><dl>
<dt><b>KRB_NT_MS_PRINICPAL</b></dt>
</dl>
</td>
<td width="60%">
Windows NT 4.0–style name.

</td>
</tr>
<tr>
<td width="40%"><a id="KRB_NT_MS_PRINCIPAL_AND_ID"></a><a id="krb_nt_ms_principal_and_id"></a><dl>
<dt><b>KRB_NT_MS_PRINCIPAL_AND_ID</b></dt>
</dl>
</td>
<td width="60%">
Windows NT 4.0–style name with SID.

</td>
</tr>
</table>
 


### -field NameCount

Indicates the number of names stored in <b>Names</b>.


### -field Names

Array of 
<a href="https://msdn.microsoft.com/4687d63a-4e58-4181-a48f-2724e5015e77">UNICODE_STRINGS</a> containing the names.

