---
UID: NS:cryptxml._CRYPT_XML_KEY_INFO
title: "_CRYPT_XML_KEY_INFO"
author: windows-sdk-content
description: Encapsulates key information data.
old-location: security\crypt_xml_key_info.htm
tech.root: SecCrypto
ms.assetid: 0fd4a80f-52c1-4ff8-9e49-87ddc1f2521d
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*PCRYPT_XML_KEY_INFO, CRYPT_XML_KEY_INFO, CRYPT_XML_KEY_INFO structure [Security], _CRYPT_XML_KEY_INFO, cryptxml/CRYPT_XML_KEY_INFO, security.crypt_xml_key_info"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Cryptxml.h
api_name:
 - CRYPT_XML_KEY_INFO
product: Windows
targetos: Windows
req.typenames: CRYPT_XML_KEY_INFO, *PCRYPT_XML_KEY_INFO
req.redist: 
---

# _CRYPT_XML_KEY_INFO structure


## -description


The <b>CRYPT_XML_KEY_INFO</b> structure encapsulates key information data.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field wszId

A pointer to a null-terminated wide character string that specifies the value of the <b>ID</b> attribute of the key information element.


### -field cKeyInfo

The number of items in the array pointed to by the <b>rgKeyInfo</b> member.


### -field rgKeyInfo

A pointer to an array of <a href="https://msdn.microsoft.com/en-us/library/Dd433856(v=VS.85).aspx">CRYPT_XML_KEY_INFO_ITEM</a> structures that contain key information.


### -field hVerifyKey

Optional. The handle of data  derived from the first key value.

