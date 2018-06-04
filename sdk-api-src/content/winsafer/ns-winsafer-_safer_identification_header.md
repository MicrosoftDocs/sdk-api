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

# _SAFER_IDENTIFICATION_HEADER structure


## -description


The <b>SAFER_IDENTIFICATION_HEADER</b> structure is used as the header for the  
<a href="https://msdn.microsoft.com/d845a750-2931-4c17-be78-92843e2bd76f">SAFER_PATHNAME_IDENTIFICATION</a>, 
<a href="https://msdn.microsoft.com/68b4b5f5-8220-4180-8243-b6f1fd7826bd">SAFER_HASH_IDENTIFICATION</a>, and 
<a href="https://msdn.microsoft.com/8f165956-9ef0-469e-a71b-f9341a347e59">SAFER_URLZONE_IDENTIFICATION</a> structures.
			


## -struct-fields




### -field dwIdentificationType


<a href="https://msdn.microsoft.com/ced40d58-e9f1-47cc-9e05-fdaa253bb16b">SAFER_IDENTIFICATION_TYPES</a> enumeration value that indicates the type of the structure. The following table shows the possible values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SaferIdentityDefault"></a><a id="saferidentitydefault"></a><a id="SAFERIDENTITYDEFAULT"></a><dl>
<dt><b>SaferIdentityDefault</b></dt>
</dl>
</td>
<td width="60%">
The header is for a default structure.

</td>
</tr>
<tr>
<td width="40%"><a id="SaferIdentityTypeImageName"></a><a id="saferidentitytypeimagename"></a><a id="SAFERIDENTITYTYPEIMAGENAME"></a><dl>
<dt><b>SaferIdentityTypeImageName</b></dt>
</dl>
</td>
<td width="60%">
The header is for a <a href="https://msdn.microsoft.com/d845a750-2931-4c17-be78-92843e2bd76f">SAFER_PATHNAME_IDENTIFICATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="SaferIdentityTypeImageHash"></a><a id="saferidentitytypeimagehash"></a><a id="SAFERIDENTITYTYPEIMAGEHASH"></a><dl>
<dt><b>SaferIdentityTypeImageHash</b></dt>
</dl>
</td>
<td width="60%">
The header is for a <a href="https://msdn.microsoft.com/68b4b5f5-8220-4180-8243-b6f1fd7826bd">SAFER_HASH_IDENTIFICATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="SaferIdentityTypeUrlZone"></a><a id="saferidentitytypeurlzone"></a><a id="SAFERIDENTITYTYPEURLZONE"></a><dl>
<dt><b>SaferIdentityTypeUrlZone</b></dt>
</dl>
</td>
<td width="60%">
The header is for a <a href="https://msdn.microsoft.com/8f165956-9ef0-469e-a71b-f9341a347e59">SAFER_URLZONE_IDENTIFICATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="SaferIdentityTypeCertificate"></a><a id="saferidentitytypecertificate"></a><a id="SAFERIDENTITYTYPECERTIFICATE"></a><dl>
<dt><b>SaferIdentityTypeCertificate</b></dt>
</dl>
</td>
<td width="60%">
The header is for a <a href="https://msdn.microsoft.com/d845a750-2931-4c17-be78-92843e2bd76f">SAFER_PATHNAME_IDENTIFICATION</a> structure.

</td>
</tr>
</table>
 


### -field cbStructSize

The size of the entire  <a href="https://msdn.microsoft.com/d845a750-2931-4c17-be78-92843e2bd76f">SAFER_PATHNAME_IDENTIFICATION</a>, 
<a href="https://msdn.microsoft.com/68b4b5f5-8220-4180-8243-b6f1fd7826bd">SAFER_HASH_IDENTIFICATION</a>, or 
<a href="https://msdn.microsoft.com/8f165956-9ef0-469e-a71b-f9341a347e59">SAFER_URLZONE_IDENTIFICATION</a> structure, including the common header.


### -field IdentificationGuid

The GUID of the identification.


### -field lastModified

 




#### - LastModified

The date and time of the last change to this identification.

