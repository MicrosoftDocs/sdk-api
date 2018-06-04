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

# CRYPT_XML_KEYINFO_SPEC enumeration


## -description


The <b>CRYPT_XML_KEYINFO_SPEC</b> enumeration specifies values for the <i>dwKeyInfoSpec</i> parameter in the <a href="https://msdn.microsoft.com/38bd365e-bc63-498c-a650-471429f09d37">CryptXmlSign</a> function.


## -enum-fields




### -field CRYPT_XML_KEYINFO_SPEC_NONE

The value of the <b>KeyInfo</b> member in the <a href="https://msdn.microsoft.com/d9930946-aec0-42a4-949f-af8b2e9c6e6c">CRYPT_XML_SIGNATURE</a> structure is null.


### -field CRYPT_XML_KEYINFO_SPEC_ENCODED

The value of the encoded <a href="https://msdn.microsoft.com/0fd4a80f-52c1-4ff8-9e49-87ddc1f2521d">CRYPT_XML_KEY_INFO</a> structure is specified in a <a href="https://msdn.microsoft.com/b70aae53-919b-4d4a-b284-ea6bc223842f">CRYPT_XML_BLOB</a> structure pointed to in the <i>pvKeyInfoSpec</i> parameter.


### -field CRYPT_XML_KEYINFO_SPEC_PARAM

The members  of the <a href="https://msdn.microsoft.com/0fd4a80f-52c1-4ff8-9e49-87ddc1f2521d">CRYPT_XML_KEY_INFO</a> structure to be encoded are specified in a <a href="https://msdn.microsoft.com/cbde3f67-d948-452a-9958-52563dc7a8b5">CRYPT_XML_KEYINFO_PARAM</a> structure pointed by the <i>pvKeyInfoSpec</i> parameter.

