---
UID: NS:cryptxml._CRYPT_XML_TRANSFORM_CHAIN_CONFIG
title: "_CRYPT_XML_TRANSFORM_CHAIN_CONFIG"
author: windows-driver-content
description: Contains application defined transforms that are allowed for use in the XML digital signature.
old-location: security\crypt_xml_transform_chain_config.htm
old-project: SecCrypto
ms.assetid: ad18ee99-685d-4a79-bd91-492df20edb8c
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: "*PCRYPT_XML_TRANSFORM_CHAIN_CONFIG, CRYPT_XML_TRANSFORM_CHAIN_CONFIG, CRYPT_XML_TRANSFORM_CHAIN_CONFIG structure [Security], PCRYPT_XML_TRANSFORM_CHAIN_CONFIG, PCRYPT_XML_TRANSFORM_CHAIN_CONFIG structure pointer [Security], _CRYPT_XML_TRANSFORM_CHAIN_CONFIG, cryptxml/CRYPT_XML_TRANSFORM_CHAIN_CONFIG, cryptxml/PCRYPT_XML_TRANSFORM_CHAIN_CONFIG, security.crypt_xml_transform_chain_config"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: cryptxml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CRYPT_XML_TRANSFORM_CHAIN_CONFIG, *PCRYPT_XML_TRANSFORM_CHAIN_CONFIG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Cryptxml.h
api_name:
-	CRYPT_XML_TRANSFORM_CHAIN_CONFIG
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _CRYPT_XML_TRANSFORM_CHAIN_CONFIG structure


## -description


The <b>CRYPT_XML_TRANSFORM_CHAIN_CONFIG</b> structure contains application defined transforms that are allowed for use  in the XML digital signature.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field cTransformInfo

The number of elements in the array pointed to by the <b>rgpTransformInfo</b> member.


### -field rgpTransformInfo

A pointer to an array of pointers to <a href="https://msdn.microsoft.com/4821dc8f-11d4-4083-bb17-9d9637d99af5">CRYPT_XML_TRANSFORM_INFO</a> structures that contain the transform parameters.

