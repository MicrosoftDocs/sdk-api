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
 

 

