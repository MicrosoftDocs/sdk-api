---
UID: NS:cryptuiapi._CRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO
title: "_CRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO"
author: windows-driver-content
description: Used with the CRYPTUI_WIZ_DIGITAL_SIGN_INFO structure to contain extended information about a signature.
old-location: security\cryptui_wiz_digital_sign_extended_info.htm
old-project: SecCrypto
ms.assetid: e061aac4-8c9f-4282-a8f8-bc0c5a10e566
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: "*PCRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO, CRYPTUI_WIZ_DIGITAL_SIGN_COMMERCIAL, CRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO, CRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO structure [Security], CRYPTUI_WIZ_DIGITAL_SIGN_INDIVIDUAL, PCRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO, PCRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO structure pointer [Security], _CRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO, cryptuiapi/CRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO, cryptuiapi/PCRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO, security.cryptui_wiz_digital_sign_extended_info"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: CRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO, *PCRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Cryptuiapi.h
api_name:
-	CRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _CRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO structure


## -description


<p class="CCE_Message">[The  <b>CRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO</b> structure is used with the <a href="https://msdn.microsoft.com/22d0bc45-0f66-4f5f-87d3-0849c4327eed">CRYPTUI_WIZ_DIGITAL_SIGN_INFO</a> structure to contain extended information about a signature.


## -struct-fields




### -field dwSize

The size, in bytes, of the structure.


### -field dwAttrFlags

A value that indicates the type of the signature. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_DIGITAL_SIGN_COMMERCIAL"></a><a id="cryptui_wiz_digital_sign_commercial"></a><dl>
<dt><b>CRYPTUI_WIZ_DIGITAL_SIGN_COMMERCIAL</b></dt>
</dl>
</td>
<td width="60%">
The signature is a commercial signature.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_DIGITAL_SIGN_INDIVIDUAL"></a><a id="cryptui_wiz_digital_sign_individual"></a><dl>
<dt><b>CRYPTUI_WIZ_DIGITAL_SIGN_INDIVIDUAL</b></dt>
</dl>
</td>
<td width="60%">
The signature is a personal signature.

</td>
</tr>
</table>
 


### -field pwszDescription

A pointer to a null-terminated Unicode string that contains the description of the subject of the signature.


### -field pwszMoreInfoLocation

A pointer to a null-terminated Unicode string that contains the location from which to get more information about the file. This information will be displayed when the file is downloaded.


### -field pszHashAlg

A pointer to a null-terminated ANSI string that contains the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) of the hash algorithm used for the signature. The default value is <b>NULL</b>, which indicates that the SHA-1 hash algorithm is used.


### -field pwszSigningCertDisplayString

A pointer to a null-terminated Unicode string that contains the string displayed on the digital signature wizard page. The string should prompt the user to select a certificate for a specific purpose.


### -field hAdditionalCertStore

A handle to an additional certificate store that will be added to the signature.


### -field psAuthenticated

A pointer to a <a href="https://msdn.microsoft.com/782f3022-d852-4ad7-8e0f-afbccc25928a">CRYPT_ATTRIBUTES</a> structure that contains authenticated attributes supplied by the user.


### -field psUnauthenticated

A pointer to a <a href="https://msdn.microsoft.com/782f3022-d852-4ad7-8e0f-afbccc25928a">CRYPT_ATTRIBUTES</a> structure that contains unauthenticated attributes supplied by the user.


## -see-also




<a href="https://msdn.microsoft.com/22d0bc45-0f66-4f5f-87d3-0849c4327eed">CRYPTUI_WIZ_DIGITAL_SIGN_INFO</a>
 

 

