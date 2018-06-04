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

# CryptEnumOIDInfo function


## -description



			The <b>CryptEnumOIDInfo</b> function enumerates predefined and registered <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) 
<a href="https://msdn.microsoft.com/06ba0f60-778d-450b-8f71-23471b8c4e2c">CRYPT_OID_INFO</a> structures. This function enumerates either all of the predefined and registered structures or only structures identified by a selected OID group. For each OID information structure enumerated, an application provided callback function, <i>pfnEnumOIDInfo</i>, is called.
		


## -parameters




### -param dwGroupId [in]

Indicates which OID groups to be matched. Setting <i>dwGroupId</i> to zero matches all groups. If <i>dwGroupId</i> is greater than zero, only the OID entries in the specified group are enumerated. 




The currently defined OID group IDs are:

<ul>
<li>CRYPT_HASH_ALG_OID_GROUP_ID</li>
<li>CRYPT_ENCRYPT_ALG_OID_GROUP_ID</li>
<li>CRYPT_PUBKEY_ALG_OID_GROUP_ID</li>
<li>CRYPT_SIGN_ALG_OID_GROUP_ID</li>
<li>CRYPT_RDN_ATTR_OID_GROUP_ID</li>
<li>CRYPT_EXT_OR_ATTR_OID_GROUP_ID</li>
<li>CRYPT_ENHKEY_USAGE_OID_GROUP_ID</li>
<li>CRYPT_POLICY_OID_GROUP_ID</li>
<li>CRYPT_TEMPLATE_OID_GROUP_ID</li>
<li>CRYPT_KDF_OID_GROUP_ID<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>The CRYPT_KDF_OID_GROUP_ID value is not supported.

</li>
<li>CRYPT_LAST_OID_GROUP_ID</li>
<li>CRYPT_FIRST_ALG_OID_GROUP_ID</li>
<li>CRYPT_LAST_ALG_OID_GROUP_ID</li>
</ul>

### -param dwFlags [in]

This parameter is reserved for future use. It must be zero.


### -param pvArg [in]

A pointer to arguments to be passed through to the callback function.


### -param pfnEnumOIDInfo [in]

A pointer to the callback function that is executed for each OID information entry enumerated. For information about the callback parameters, see <a href="https://msdn.microsoft.com/30ae4274-631d-4c6a-96c5-18f096607cad">CRYPT_ENUM_OID_INFO</a>.


## -returns




						If the callback function  completes the enumeration, this function returns <b>TRUE</b>. 

If the callback function has stopped the enumeration, this function returns <b>FALSE</b>.




## -see-also




<a href="cryptography_functions.htm">OID Support Functions</a>
 

 

