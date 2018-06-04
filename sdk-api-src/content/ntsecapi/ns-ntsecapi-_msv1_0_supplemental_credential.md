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

# _MSV1_0_SUPPLEMENTAL_CREDENTIAL structure


## -description



			The <b>MSV1_0_SUPPLEMENTAL_CREDENTIAL</b> structure is used to pass <a href="https://msdn.microsoft.com/library/windows/hardware/dn922689">credentials</a> into MSV1_0 from <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">Kerberos</a> or custom <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">authentication package</a>.


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

Contains the  LM password. The size of this array is defined by the constant <b>MSV1_0_OWF_PASSWORD_LENGTH</b>. When you have finished using the password, remove the sensitive information from memory by calling <a href="https://msdn.microsoft.com/2c4090a6-025b-4b7b-8f31-7e744ad51b39">SecureZeroMemory</a>. For more information on protecting the password, see <a href="https://msdn.microsoft.com/1d810f71-9bf5-4c5c-a573-c35081f604cf">Handling Passwords</a>.


### -field NtPassword

A string that contains the Windows password. The size of this array is defined by the constant <b>MSV1_0_OWF_PASSWORD_LENGTH</b>. When you have finished using the password, remove the sensitive information from memory by calling <a href="https://msdn.microsoft.com/2c4090a6-025b-4b7b-8f31-7e744ad51b39">SecureZeroMemory</a>.

