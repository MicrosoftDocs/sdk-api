---
UID: NS:cryptxml._CRYPT_XML_BLOB
title: "_CRYPT_XML_BLOB"
author: windows-sdk-content
description: Contains an arbitrary array of bytes.
old-location: security\crypt_xml_blob.htm
tech.root: seccrypto
ms.assetid: b70aae53-919b-4d4a-b284-ea6bc223842f
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: "*PCRYPT_XML_BLOB, CRYPT_XML_BLOB, CRYPT_XML_BLOB structure [Security], PCRYPT_XML_BLOB, PCRYPT_XML_BLOB structure pointer [Security], _CRYPT_XML_BLOB, cryptxml/CRYPT_XML_BLOB, cryptxml/PCRYPT_XML_BLOB, security.crypt_xml_blob"
ms.prod: windows
ms.technology: windows-sdk
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
 - CRYPT_XML_BLOB
product: Windows
targetos: Windows
req.typenames: CRYPT_XML_BLOB, *PCRYPT_XML_BLOB
req.redist: 
---

# _CRYPT_XML_BLOB structure


## -description


The <b>CRYPT_XML_BLOB</b> structure contains an arbitrary array of bytes. 


## -struct-fields




### -field dwCharset

Specifies the character set used to encode the signature.


### -field cbData

The size, in bytes, of this structure.

Range: 0–CRYPT_XML_BLOB_MAX) (value is 0x7FFFFFF8)


### -field pbData

A pointer to encoded XML data.

