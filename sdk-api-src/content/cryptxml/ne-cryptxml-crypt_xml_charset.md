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

# CRYPT_XML_CHARSET enumeration


## -description


The <b>CRYPT_XML_CHARSET</b> enumeration is used to specify the character set used in the XML.


## -enum-fields




### -field CRYPT_XML_CHARSET_AUTO

This value is only supported in the <a href="https://msdn.microsoft.com/b6a77d62-b92d-4b83-949f-14a0ce3ce025">CryptXmlOpenToDecode</a> function. The encoded XML character set is determined by the parser and is based on the XML declaration or the best guess on the characters.


### -field CRYPT_XML_CHARSET_UTF8

Specifies the UTF-8 character set.


### -field CRYPT_XML_CHARSET_UTF16LE

Specifies the UTF-16 little-endian character set.


### -field CRYPT_XML_CHARSET_UTF16BE

Specifies the UTF-16 big-endian character set.

