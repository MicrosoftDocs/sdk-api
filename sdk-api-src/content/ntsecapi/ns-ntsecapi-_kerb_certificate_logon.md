---
UID: NS:ntsecapi._KERB_CERTIFICATE_LOGON
title: "_KERB_CERTIFICATE_LOGON"
author: windows-driver-content
description: Contains information about a smart card logon session.
old-location: security\kerb_certificate_logon.htm
old-project: SecAuthN
ms.assetid: e6aa0042-edb5-4e9b-b545-5159d3bfb8fc
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: "*PKERB_CERTIFICATE_LOGON, KERB_CERTIFICATE_LOGON, KERB_CERTIFICATE_LOGON structure [Security], KERB_CERTIFICATE_LOGON_FLAG_CHECK_DUPLICATES, KERB_CERTIFICATE_LOGON_FLAG_USE_CERTIFICATE_INFO, KerbCertificateLogon, KerbCertificateUnlockLogon, PKERB_CERTIFICATE_LOGON, PKERB_CERTIFICATE_LOGON structure pointer [Security], _KERB_CERTIFICATE_LOGON, ntsecapi/KERB_CERTIFICATE_LOGON, ntsecapi/PKERB_CERTIFICATE_LOGON, security.kerb_certificate_logon"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: KERB_CERTIFICATE_LOGON, *PKERB_CERTIFICATE_LOGON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntsecapi.h
api_name:
-	KERB_CERTIFICATE_LOGON
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# _KERB_CERTIFICATE_LOGON structure


## -description


The <b>KERB_CERTIFICATE_LOGON</b> structure contains information about a smart card <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">logon session</a>.

It is passed as the <i>AuthenticationInformation</i> parameter to the 
<a href="https://msdn.microsoft.com/75968d53-5af2-4d77-9486-26403b73c954">LsaLogonUser</a> function when the <a href="https://msdn.microsoft.com/43970c99-53f1-43c1-9d9f-65573572f731">Kerberos</a> security package performs an interactive smart card logon.


## -struct-fields




### -field MessageType

A member of the <a href="https://msdn.microsoft.com/500bee53-638b-4782-b42d-1df158396fb6">KERB_LOGON_SUBMIT_TYPE</a> enumeration that indicates how this structure is used. The member must be one of the following values.

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
<a href="https://msdn.microsoft.com/75968d53-5af2-4d77-9486-26403b73c954">LsaLogonUser</a> function to perform an interactive smart card logon.

</td>
</tr>
<tr>
<td width="40%"><a id="KerbCertificateUnlockLogon"></a><a id="kerbcertificateunlocklogon"></a><a id="KERBCERTIFICATEUNLOCKLOGON"></a><dl>
<dt><b>KerbCertificateUnlockLogon</b></dt>
<dt>15</dt>
</dl>
</td>
<td width="60%">
This structure is used as the <b>Logon</b> member of a <a href="https://msdn.microsoft.com/04e058b0-9a05-4ed7-9d4a-1c8c003d8077">KERB_CERTIFICATE_UNLOCK_LOGON</a> structure.

</td>
</tr>
</table>
 


### -field DomainName

The domain name of the user to authenticate. The value of this member can be empty. If the value is not empty, <a href="https://msdn.microsoft.com/75968d53-5af2-4d77-9486-26403b73c954">LsaLogonUser</a> uses the value to locate the <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">Key Distribution Center</a> (KDC). If the value is empty, <b>LsaLogonUser</b> attempts to authenticate against the domain to which the computer is joined.  The pointer is relative to the beginning of the structure and is not an absolute memory pointer.


### -field UserName

The user name of the user to authenticate. The value of this member can be empty. If the value is not empty, <a href="https://msdn.microsoft.com/75968d53-5af2-4d77-9486-26403b73c954">LsaLogonUser</a> uses the value to locate the user account to authenticate.  The pointer is relative to the beginning of the structure and is not an absolute memory pointer.


### -field Pin

The PIN to use to authenticate the user. The <b>Length</b> member of this structure does not include the terminating null character of the PIN. The pointer is relative to the beginning of the structure and is not an absolute memory pointer.

The PIN can be protected by using the <a href="https://msdn.microsoft.com/1e299dfb-2ffe-463c-9e2c-b7774a2216e3">CredProtect</a> function.


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

A pointer to a <a href="https://msdn.microsoft.com/b3e6722a-25dd-4137-b224-4082e846ddec">KERB_SMARTCARD_CSP_INFO</a> structure that contains information about the smart card <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) ) or a pointer to a marshaled <a href="https://msdn.microsoft.com/1E8CA0FE-02DF-4FAA-B0ED-5882DF38B78A">KERB_CERTIFICATE_INFO</a> structure when updating certificate credentials.


## -remarks



This structure, along with the data pointed to by the <b>DomainName</b>, <b>UserName</b>, <b>Pin</b>, and <b>CspData</b> members, is contained in a single block of contiguous memory. When this structure is serialized, the offsets specified by each of these members must be multiples of two.

The pointers stored in the members of <b>UNICODE_STRING</b> type are relative to the beginning of the structure and are not absolute memory pointers.




## -see-also




<a href="https://msdn.microsoft.com/04e058b0-9a05-4ed7-9d4a-1c8c003d8077">KERB_CERTIFICATE_UNLOCK_LOGON</a>



<a href="https://msdn.microsoft.com/b3e6722a-25dd-4137-b224-4082e846ddec">KERB_SMARTCARD_CSP_INFO</a>



<a href="https://msdn.microsoft.com/75968d53-5af2-4d77-9486-26403b73c954">LsaLogonUser</a>
 

 

