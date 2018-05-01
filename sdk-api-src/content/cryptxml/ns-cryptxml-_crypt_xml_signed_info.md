---
UID: NS:cryptxml._CRYPT_XML_SIGNED_INFO
title: "_CRYPT_XML_SIGNED_INFO"
author: windows-driver-content
description: Describes an XML encoded SignedInfo element.
old-location: security\crypt_xml_signed_info.htm
old-project: SecCrypto
ms.assetid: 34f7f3be-8bf8-4863-9c94-79ee14a7ebea
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: "*PCRYPT_XML_SIGNED_INFO, CRYPT_XML_SIGNED_INFO, CRYPT_XML_SIGNED_INFO structure [Security], PCRYPT_XML_SIGNED_INFO, PCRYPT_XML_SIGNED_INFO structure pointer [Security], _CRYPT_XML_SIGNED_INFO, cryptxml/CRYPT_XML_SIGNED_INFO, cryptxml/PCRYPT_XML_SIGNED_INFO, security.crypt_xml_signed_info"
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
req.typenames: CRYPT_XML_SIGNED_INFO, *PCRYPT_XML_SIGNED_INFO, CRYPT_XML_SIGNED_INFO, *PCRYPT_XML_SIGNED_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Cryptxml.h
api_name:
-	CRYPT_XML_SIGNED_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _CRYPT_XML_SIGNED_INFO structure


## -description


The <b>CRYPT_XML_SIGNED_INFO</b> structure describes an XML encoded <b>SignedInfo</b> element.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field wszId

Optional.  A pointer to a null-terminated Unicode string that contains the <b>Id</b> attribute. 


### -field Canonicalization

A <a href="https://msdn.microsoft.com/4eb99c1e-fa06-41ec-906c-a3ba34e7aaeb">CRYPT_XML_ALGORITHM</a> structure that specifies the canonicalization algorithm.


### -field SignatureMethod

A <a href="https://msdn.microsoft.com/4eb99c1e-fa06-41ec-906c-a3ba34e7aaeb">CRYPT_XML_ALGORITHM</a> structure that specifies the signature algorithm.


### -field cReference

The number of elements in the array pointed to by the <b>rgpReference</b> member.


### -field rgpReference

A pointer to an array of pointers to <a href="https://msdn.microsoft.com/af16af5a-b1e5-4250-bdb1-f3fceb1830b9">CRYPT_XML_REFERENCE</a> structures   that contain information that is encoded in <b>Reference</b> elements.


### -field Encoded

A  <a href="https://msdn.microsoft.com/b70aae53-919b-4d4a-b284-ea6bc223842f">CRYPT_XML_BLOB</a> structure that contains the XML encoded <b>SignedInfo</b> element.

