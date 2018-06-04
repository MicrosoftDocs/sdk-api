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

# _KERB_CERTIFICATE_S4U_LOGON structure


## -description


The <b>KERB_CERTIFICATE_S4U_LOGON</b> structure contains information about the certificate for a service for user (S4U) logon.


## -struct-fields




### -field MessageType

A value of the <a href="https://msdn.microsoft.com/500bee53-638b-4782-b42d-1df158396fb6">KERB_LOGON_SUBMIT_TYPE</a> enumeration that identifies the type of logon request being made. This member must be set to <b>KerbCertificateS4ULogon</b>. 


### -field Flags

Flags that provide more information about the certificate logon.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="KERB_CERTIFICATE_S4U_LOGON_FLAG_CHECK_DUPLICATES"></a><a id="kerb_certificate_s4u_logon_flag_check_duplicates"></a><dl>
<dt><b>KERB_CERTIFICATE_S4U_LOGON_FLAG_CHECK_DUPLICATES</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/f2a7c87c-9be7-4fd8-8ecd-4edf1f2336ef">Key Distribution Center</a> (KDC) checks for account mapping conflicts for the same certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_CERTIFICATE_S4U_LOGON_FLAG_CHECK_LOGONHOURS"></a><a id="kerb_certificate_s4u_logon_flag_check_logonhours"></a><dl>
<dt><b>KERB_CERTIFICATE_S4U_LOGON_FLAG_CHECK_LOGONHOURS</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
The KDC checks the length of time this account with this certificate has been logged on.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_CERTIFICATE_S4U_LOGON_FLAG_IF_NT_AUTH_POLICY_REQUIRED"></a><a id="kerb_certificate_s4u_logon_flag_if_nt_auth_policy_required"></a><dl>
<dt><b>KERB_CERTIFICATE_S4U_LOGON_FLAG_IF_NT_AUTH_POLICY_REQUIRED</b></dt>
<dt>0x4</dt>
</dl>
</td>
<td width="60%">
The KDC checks to see if an authentication policy is set.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_CERTIFICATE_S4U_LOGON_FLAG_IDENTIFY"></a><a id="kerb_certificate_s4u_logon_flag_identify"></a><dl>
<dt><b>KERB_CERTIFICATE_S4U_LOGON_FLAG_IDENTIFY</b></dt>
<dt>0x8</dt>
</dl>
</td>
<td width="60%">
The KDC checks for identity only tokens instead of impersonation tokens. The request for the identity token must have the same value as the <b>KERB_S4U_LOGON_FLAG_IDENTIFY</b> flag in the <a href="https://msdn.microsoft.com/ab94c36b-7aba-452d-abc0-220c91ffacca">KERB_S4U_LOGON</a> structure.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista with SP2:  </b>This flag is not available.

</td>
</tr>
</table>
 


### -field UserPrincipalName

The user principal name of the client to authenticate. The value of this member can be <b>NULL</b>.   If the value is not <b>NULL</b>, the <a href="https://msdn.microsoft.com/75968d53-5af2-4d77-9486-26403b73c954">LsaLogonUser</a> function uses the value to locate the user name.


### -field DomainName

The domain name of the user to authenticate. The value of this member can be <b>NULL</b>. If the value is not <b>NULL</b>, the <a href="https://msdn.microsoft.com/75968d53-5af2-4d77-9486-26403b73c954">LsaLogonUser</a> function uses the value to locate the KDC. If the value is <b>NULL</b>, the <b>LsaLogonUser</b> function attempts to authenticate against the domain to which the computer is joined.


### -field CertificateLength

The length, in bytes, of the client certificate.


### -field Certificate

The certificate of the S4U logon.

