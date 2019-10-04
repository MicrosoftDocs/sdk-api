---
UID: NS:ntsecapi._MSV1_0_SUPPLEMENTAL_CREDENTIAL
title: MSV1_0_SUPPLEMENTAL_CREDENTIAL (ntsecapi.h)
author: windows-sdk-content
description: The MSV1_0_SUPPLEMENTAL_CREDENTIAL structure is used to pass credentials into MSV1_0 from Kerberos or custom authentication package.
old-location: security\msv1_0_supplemental_credential.htm
tech.root: SecAuthN
ms.assetid: 63848b26-b611-4ae6-8bc3-fc124a825d3d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PMSV1_0_SUPPLEMENTAL_CREDENTIAL, MSV1_0_CRED_LM_PRESENT, MSV1_0_CRED_NT_PRESENT, MSV1_0_CRED_VERSION, MSV1_0_SUPPLEMENTAL_CREDENTIAL, MSV1_0_SUPPLEMENTAL_CREDENTIAL structure [Security], PMSV1_0_SUPPLEMENTAL_CREDENTIAL, PMSV1_0_SUPPLEMENTAL_CREDENTIAL structure pointer [Security], _lsa_msv1_0_supplemental_credential, ntsecapi/MSV1_0_SUPPLEMENTAL_CREDENTIAL, ntsecapi/PMSV1_0_SUPPLEMENTAL_CREDENTIAL, security.msv1_0_supplemental_credential"
ms.topic: struct
f1_keywords: 
 - "ntsecapi/MSV1_0_SUPPLEMENTAL_CREDENTIAL"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - MSV1_0_SUPPLEMENTAL_CREDENTIAL
targetos: Windows
req.typenames: MSV1_0_SUPPLEMENTAL_CREDENTIAL, *PMSV1_0_SUPPLEMENTAL_CREDENTIAL
req.redist: 
ms.custom: 19H1
---

# MSV1_0_SUPPLEMENTAL_CREDENTIAL structure


## -description


The <b>MSV1_0_SUPPLEMENTAL_CREDENTIAL</b> structure is used to pass <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">credentials</a> into MSV1_0 from <a href="https://docs.microsoft.com/windows/desktop/SecGloss/k-gly">Kerberos</a> or custom <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">authentication package</a>.


## -struct-fields




### -field Version

Specifies the version number of the credential structure and related credential content.


### -field Flags

Describes the credential. This can contain one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSV1_0_CRED_LM_PRESENT"></a><a id="msv1_0_cred_lm_present"></a><dl>
<dt><b>MSV1_0_CRED_LM_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The credential contains a LAN Manager (LM) password stored in the <b>LmPassword</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="MSV1_0_CRED_NT_PRESENT"></a><a id="msv1_0_cred_nt_present"></a><dl>
<dt><b>MSV1_0_CRED_NT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The credential contains a Windows password stored in the <b>NtPassword</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="MSV1_0_CRED_VERSION"></a><a id="msv1_0_cred_version"></a><dl>
<dt><b>MSV1_0_CRED_VERSION</b></dt>
</dl>
</td>
<td width="60%">
Version information is included and is stored in the <b>Version</b> member.

</td>
</tr>
</table>
 


### -field LmPassword

Contains the  LM password. The size of this array is defined by the constant <b>MSV1_0_OWF_PASSWORD_LENGTH</b>. When you have finished using the password, remove the sensitive information from memory by calling <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a>. For more information on protecting the password, see <a href="https://docs.microsoft.com/windows/desktop/SecBP/handling-passwords">Handling Passwords</a>.


### -field NtPassword

A string that contains the Windows password. The size of this array is defined by the constant <b>MSV1_0_OWF_PASSWORD_LENGTH</b>. When you have finished using the password, remove the sensitive information from memory by calling <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a>.

