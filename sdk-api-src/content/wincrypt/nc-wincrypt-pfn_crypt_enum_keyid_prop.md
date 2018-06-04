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

# PFN_CRYPT_ENUM_KEYID_PROP callback function


## -description


The <b>CRYPT_ENUM_KEYID_PROP</b> callback function  is used with the <a href="https://msdn.microsoft.com/6e57d935-4cfb-44af-b1c6-6c399c959452">CryptEnumKeyIdentifierProperties</a> function.


## -parameters




### -param *pKeyIdentifier [in]

A pointer to a <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a> that contains the key identifier.


### -param dwFlags [in]

Reserved for future use and must be zero.


### -param *pvReserved [in]

Reserved for future use. Must be <b>NULL</b>.


### -param *pvArg [in, out]

A pointer to an argument that is passed back from the callback function.


### -param cProp [in]

Count of elements in the array of <i>rgdwPropId</i>


### -param *rgdwPropId [in]

A pointer to an array of property identifiers. Each entry in the array will be one of the value types listed for in the table for <i>dwPropId</i> in the <a href="https://msdn.microsoft.com/0970aaaa-3f9a-4471-bd21-5de8746f94a2">CryptSetKeyIdentifierProperty</a> function.


#### - **rgpvData [in]

A pointer to an array that contains pointers to <i>pvData</i> elements corresponding the <i>rgdwPropId</i> array elements. 




For CERT_KEY_PROV_INFO_PROP_ID the <i>rgpvData</i> element points to a <a href="https://msdn.microsoft.com/6aea2f47-9d4a-4069-ac6d-f28907df00be">CRYPT_KEY_PROV_INFO</a> structure. For all other properties, the <i>rgpvData</i> element points to an array of bytes.


### -param *rgcbData [in]

Array of <b>DWORD</b>s that specify the size, in bytes, of corresponding elements in the <i>rgpvData</i> array.


#### - rgpvData [in]

A pointer to an array that contains pointers to <i>pvData</i> elements corresponding the <i>rgdwPropId</i> array elements. 




For CERT_KEY_PROV_INFO_PROP_ID the <i>rgpvData</i> element points to a <a href="https://msdn.microsoft.com/6aea2f47-9d4a-4069-ac6d-f28907df00be">CRYPT_KEY_PROV_INFO</a> structure. For all other properties, the <i>rgpvData</i> element points to an array of bytes.


## -returns



Returns <b>TRUE</b> if the function succeeds, <b>FALSE</b> if it fails.




## -see-also




<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a>



<a href="https://msdn.microsoft.com/6aea2f47-9d4a-4069-ac6d-f28907df00be">CRYPT_KEY_PROV_INFO</a>



<a href="https://msdn.microsoft.com/6e57d935-4cfb-44af-b1c6-6c399c959452">CryptEnumKeyIdentifierProperties</a>



<a href="https://msdn.microsoft.com/0970aaaa-3f9a-4471-bd21-5de8746f94a2">CryptSetKeyIdentifierProperty</a>
 

 

