---
UID: NS:cryptuiapi._CRYPTUI_WIZ_DIGITAL_SIGN_CERT_PVK_INFO
title: "_CRYPTUI_WIZ_DIGITAL_SIGN_CERT_PVK_INFO"
author: windows-sdk-content
description: Contains information about the PVK file that contains the certificates used by the CryptUIWizDigitalSign function.
old-location: security\cryptui_wiz_digital_sign_cert_pvk_info.htm
tech.root: seccrypto
ms.assetid: 0316ed0b-d4e5-4102-9ab0-637e96c7d9f5
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: "*PCRYPTUI_WIZ_DIGITAL_SIGN_CERT_PVK_INFO, CRYPTUI_WIZ_DIGITAL_SIGN_CERT_PVK_INFO, CRYPTUI_WIZ_DIGITAL_SIGN_CERT_PVK_INFO structure [Security], CRYPTUI_WIZ_DIGITAL_SIGN_PVK_FILE, CRYPTUI_WIZ_DIGITAL_SIGN_PVK_PROV, PCRYPTUI_WIZ_DIGITAL_SIGN_CERT_PVK_INFO, PCRYPTUI_WIZ_DIGITAL_SIGN_CERT_PVK_INFO structure pointer [Security], _CRYPTUI_WIZ_DIGITAL_SIGN_CERT_PVK_INFO, cryptuiapi/CRYPTUI_WIZ_DIGITAL_SIGN_CERT_PVK_INFO, cryptuiapi/PCRYPTUI_WIZ_DIGITAL_SIGN_CERT_PVK_INFO, security.cryptui_wiz_digital_sign_cert_pvk_info"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: cryptuiapi.h
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
 - Cryptuiapi.h
api_name:
 - CRYPTUI_WIZ_DIGITAL_SIGN_CERT_PVK_INFO
product: Windows
targetos: Windows
req.typenames: CRYPTUI_WIZ_DIGITAL_SIGN_CERT_PVK_INFO, *PCRYPTUI_WIZ_DIGITAL_SIGN_CERT_PVK_INFO
req.redist: 
---

# _CRYPTUI_WIZ_DIGITAL_SIGN_CERT_PVK_INFO structure


## -description


<p class="CCE_Message">[The  <b>CRYPTUI_WIZ_DIGITAL_SIGN_CERT_PVK_INFO</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPTUI_WIZ_DIGITAL_SIGN_CERT_PVK_INFO</b> structure contains information about the PVK file that contains the certificates used by the <a href="https://msdn.microsoft.com/en-us/library/Aa380292(v=VS.85).aspx">CryptUIWizDigitalSign</a> function.


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

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/Aa380682(v=VS.85).aspx">CRYPTUI_WIZ_DIGITAL_SIGN_PVK_FILE_INFO</a> structure that contains the PVK file that contains the certificates. This member is used if <b>CRYPTUI_WIZ_DIGITAL_SIGN_PVK_FILE</b> is specified for the <b>dwPvkChoice</b> member.


### -field pPvkProvInfo

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/Aa381420(v=VS.85).aspx">CRYPT_KEY_PROV_INFO</a> structure that contains information about the PVK provider that contains the certificates. This member is used if <b>CRYPTUI_WIZ_DIGITAL_SIGN_PVK_PROV</b> is specified for the <b>dwPvkChoice</b> member.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa380292(v=VS.85).aspx">CryptUIWizDigitalSign</a>
 

 

