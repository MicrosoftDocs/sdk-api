---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _KERB_S4U_LOGON structure


## -description


The <b>KERB_S4U_LOGON</b> structure contains information about a service for user (S4U) logon. This structure is used by the <a href="https://msdn.microsoft.com/75968d53-5af2-4d77-9486-26403b73c954">LsaLogonUser</a> function with the <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">Kerberos</a> package.


## -struct-fields




### -field MessageType

A value of the <a href="https://msdn.microsoft.com/500bee53-638b-4782-b42d-1df158396fb6">KERB_LOGON_SUBMIT_TYPE</a> enumeration that identifies the type of logon being requested. This member must be set to <b>KerbS4ULogon</b>.


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
<td width="40%"><a id="KERB_S4U_LOGON_FLAG_IDENTITY"></a><a id="kerb_s4u_logon_flag_identity"></a><dl>
<dt><b>KERB_S4U_LOGON_FLAG_IDENTITY</b></dt>
<dt>0x8</dt>
</dl>
</td>
<td width="60%">
Requests the identity token.

</td>
</tr>
</table>
 


### -field ClientUpn

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> that specifies the <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">user principal name</a> (UPN) of the client. This member cannot be <b>NULL</b>.

The <b>Buffer</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> structure must point to memory that is contiguous to the <b>KERB_S4U_LOGON</b> structure.


### -field ClientRealm

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> that specifies the realm of the client, if known. If the realm is not known, this member can be <b>NULL</b>.

The <b>Buffer</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> structure must point to memory that is contiguous to the <b>KERB_S4U_LOGON</b> structure.

