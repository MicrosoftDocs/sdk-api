---
UID: NE:cryptxml.CRYPT_XML_KEYINFO_SPEC
title: CRYPT_XML_KEYINFO_SPEC
author: windows-sdk-content
description: Specifies values for the dwKeyInfoSpec parameter in the CryptXmlSign function.
old-location: security\crypt_xml_keyinfo_spec.htm
tech.root: SecCrypto
ms.assetid: 83467875-1ccf-4c02-9b0a-6faf7305950e
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: CRYPT_XML_KEYINFO_SPEC, CRYPT_XML_KEYINFO_SPEC enumeration [Security], CRYPT_XML_KEYINFO_SPEC_ENCODED, CRYPT_XML_KEYINFO_SPEC_NONE, CRYPT_XML_KEYINFO_SPEC_PARAM, cryptxml/CRYPT_XML_KEYINFO_SPEC, cryptxml/CRYPT_XML_KEYINFO_SPEC_ENCODED, cryptxml/CRYPT_XML_KEYINFO_SPEC_NONE, cryptxml/CRYPT_XML_KEYINFO_SPEC_PARAM, security.crypt_xml_keyinfo_spec
ms.prod: windows
ms.technology: windows-sdk
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
 - CRYPT_XML_KEYINFO_SPEC
product: Windows
targetos: Windows
req.typenames: CRYPT_XML_KEYINFO_SPEC
req.redist: 
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

