---
UID: NS:cryptxml._CRYPT_XML_KEY_DSA_KEY_VALUE
title: "_CRYPT_XML_KEY_DSA_KEY_VALUE"
author: windows-sdk-content
description: Defines a Digital Signature Algorithm (DSA) key value. The CRYPT_XML_KEY_DSA_KEY_VALUE structure is used as an element of the key value union in the CRYPT_XML_KEY_VALUE structure.
old-location: security\crypt_xml_key_dsa_key_value.htm
tech.root: seccrypto
ms.assetid: 634c47c2-28ba-40ea-975d-95f5663eb0b0
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: CRYPT_XML_KEY_DSA_KEY_VALUE, CRYPT_XML_KEY_DSA_KEY_VALUE structure [Security], _CRYPT_XML_KEY_DSA_KEY_VALUE, cryptxml/CRYPT_XML_KEY_DSA_KEY_VALUE, security.crypt_xml_key_dsa_key_value
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
 - CRYPT_XML_KEY_DSA_KEY_VALUE
product: Windows
targetos: Windows
req.typenames: CRYPT_XML_KEY_DSA_KEY_VALUE
req.redist: 
---

# _CRYPT_XML_KEY_DSA_KEY_VALUE structure


## -description


The <b>CRYPT_XML_KEY_DSA_KEY_VALUE</b> structure defines a <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Digital Signature Algorithm</a> (DSA) key value.  The <b>CRYPT_XML_KEY_DSA_KEY_VALUE</b> structure is used as an element of the key value union  in the <a href="https://msdn.microsoft.com/en-us/library/Dd433858(v=VS.85).aspx">CRYPT_XML_KEY_VALUE</a> structure.


## -struct-fields




### -field P

Defines the  P part of the DSA key.


### -field Q

Defines the  Q part of the DSA key.


### -field G

Defines the  G part of the DSA key.


### -field Y

Defines the Y  part of the DSA key.


### -field J

Defines the J part of the DSA key.


### -field Seed

The seed value, in big-endian format.


### -field Counter

The count value, in big-endian format.

