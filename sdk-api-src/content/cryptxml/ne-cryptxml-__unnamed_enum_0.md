---
UID: NE:cryptxml.__unnamed_enum_0
title: CRYPT_XML_CHARSET
author: windows-sdk-content
description: Used to specify the character set used in the XML.
old-location: security\crypt_xml_charset.htm
tech.root: seccrypto
ms.assetid: 3f115ac1-a8ed-4151-b3f3-7ddb695802a0
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: CRYPT_XML_CHARSET, CRYPT_XML_CHARSET enumeration [Security], CRYPT_XML_CHARSET_AUTO, CRYPT_XML_CHARSET_UTF16BE, CRYPT_XML_CHARSET_UTF16LE, CRYPT_XML_CHARSET_UTF8, cryptxml/CRYPT_XML_CHARSET, cryptxml/CRYPT_XML_CHARSET_AUTO, cryptxml/CRYPT_XML_CHARSET_UTF16BE, cryptxml/CRYPT_XML_CHARSET_UTF16LE, cryptxml/CRYPT_XML_CHARSET_UTF8, security.crypt_xml_charset
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
 - CRYPT_XML_CHARSET
product: Windows
targetos: Windows
req.typenames: CRYPT_XML_CHARSET
req.redist: 
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

