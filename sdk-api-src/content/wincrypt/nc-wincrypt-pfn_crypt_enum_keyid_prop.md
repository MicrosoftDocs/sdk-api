---
UID: NC:wincrypt.PFN_CRYPT_ENUM_KEYID_PROP
title: PFN_CRYPT_ENUM_KEYID_PROP (wincrypt.h)
author: windows-sdk-content
description: The CRYPT_ENUM_KEYID_PROP callback function is used with the CryptEnumKeyIdentifierProperties function.
old-location: security\crypt_enum_keyid_prop.htm
tech.root: SecCrypto
ms.assetid: c4461b79-d216-4d4a-bd5d-9260ec897c14
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CRYPT_ENUM_KEYID_PROP, CRYPT_ENUM_KEYID_PROP callback function [Security], PFN_CRYPT_ENUM_KEYID_PROP, PFN_CRYPT_ENUM_KEYID_PROP callback, security.crypt_enum_keyid_prop, wincrypt/CRYPT_ENUM_KEYID_PROP
ms.topic: callback
req.header: wincrypt.h
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
 - UserDefined
api_location:
 - Wincrypt.h
api_name:
 - CRYPT_ENUM_KEYID_PROP
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

