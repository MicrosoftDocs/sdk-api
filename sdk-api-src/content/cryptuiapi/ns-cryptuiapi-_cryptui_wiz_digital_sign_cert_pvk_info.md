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

# _CRYPTUI_WIZ_DIGITAL_SIGN_CERT_PVK_INFO structure


## -description


<p class="CCE_Message">[The  <b>CRYPTUI_WIZ_DIGITAL_SIGN_CERT_PVK_INFO</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPTUI_WIZ_DIGITAL_SIGN_CERT_PVK_INFO</b> structure contains information about the PVK file that contains the certificates used by the <a href="https://msdn.microsoft.com/1d01523e-d47b-49be-82c8-5e98f97be800">CryptUIWizDigitalSign</a> function.


## -struct-fields




### -field dwSize

The size, in bytes, of the structure.


### -field pwszSigningCertFileName

A pointer to a null-terminated Unicode string that contains the path and file named of the file that contains the signing certificates.


### -field dwPvkChoice

Specifies the type of entity that contains the certificates. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_DIGITAL_SIGN_PVK_FILE"></a><a id="cryptui_wiz_digital_sign_pvk_file"></a><dl>
<dt><b>CRYPTUI_WIZ_DIGITAL_SIGN_PVK_FILE</b></dt>
</dl>
</td>
<td width="60%">
The entity is a PVK file.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_DIGITAL_SIGN_PVK_PROV"></a><a id="cryptui_wiz_digital_sign_pvk_prov"></a><dl>
<dt><b>CRYPTUI_WIZ_DIGITAL_SIGN_PVK_PROV</b></dt>
</dl>
</td>
<td width="60%">
The entity is a PVK provider.

</td>
</tr>
</table>
 


### -field pPvkFileInfo

A pointer to a <a href="https://msdn.microsoft.com/0e737661-2cc3-47be-ab32-0efbc18fefbd">CRYPTUI_WIZ_DIGITAL_SIGN_PVK_FILE_INFO</a> structure that contains the PVK file that contains the certificates. This member is used if <b>CRYPTUI_WIZ_DIGITAL_SIGN_PVK_FILE</b> is specified for the <b>dwPvkChoice</b> member.


### -field pPvkProvInfo

A pointer to a <a href="https://msdn.microsoft.com/6aea2f47-9d4a-4069-ac6d-f28907df00be">CRYPT_KEY_PROV_INFO</a> structure that contains information about the PVK provider that contains the certificates. This member is used if <b>CRYPTUI_WIZ_DIGITAL_SIGN_PVK_PROV</b> is specified for the <b>dwPvkChoice</b> member.


## -see-also




<a href="https://msdn.microsoft.com/1d01523e-d47b-49be-82c8-5e98f97be800">CryptUIWizDigitalSign</a>
 

 

