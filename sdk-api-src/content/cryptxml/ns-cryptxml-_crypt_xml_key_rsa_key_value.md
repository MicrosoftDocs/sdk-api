---
UID: NS:cryptxml._CRYPT_XML_KEY_RSA_KEY_VALUE
title: "_CRYPT_XML_KEY_RSA_KEY_VALUE"
author: windows-sdk-content
description: Defines an RSA key value. The CRYPT_XML_KEY_RSA_KEY_VALUE structure is used as element of the key value union in the CRYPT_XML_KEY_VALUE structure.
old-location: security\crypt_xml_key_rsa_key_value.htm
old-project: SecCrypto
ms.assetid: e2b1344d-c108-4255-bd50-06d742ed67a8
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: CRYPT_XML_KEY_RSA_KEY_VALUE, CRYPT_XML_KEY_RSA_KEY_VALUE structure [Security], _CRYPT_XML_KEY_RSA_KEY_VALUE, cryptxml/CRYPT_XML_KEY_RSA_KEY_VALUE, security.crypt_xml_key_rsa_key_value
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
tech.root: 
req.typenames: CRYPT_XML_KEY_RSA_KEY_VALUE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Cryptxml.h
api_name:
-	CRYPT_XML_KEY_RSA_KEY_VALUE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _CRYPT_XML_KEY_RSA_KEY_VALUE structure


## -description


The <b>CRYPT_XML_KEY_RSA_KEY_VALUE</b> structure defines an RSA key value.  The <b>CRYPT_XML_KEY_RSA_KEY_VALUE</b> structure is used as element of the key value union  in the <a href="https://msdn.microsoft.com/7aadd268-41bc-4ba3-babb-2ca7b13f378b">CRYPT_XML_KEY_VALUE</a> structure.


## -struct-fields




### -field Modulus

A <a href="https://msdn.microsoft.com/dc7e23d6-923c-40d2-9cf7-9a529c0634ce">CRYPT_XML_DATA_BLOB</a> structure that contains the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a> modulus data.


### -field Exponent

A <a href="https://msdn.microsoft.com/dc7e23d6-923c-40d2-9cf7-9a529c0634ce">CRYPT_XML_DATA_BLOB</a> structure that contains the public key exponent data.

