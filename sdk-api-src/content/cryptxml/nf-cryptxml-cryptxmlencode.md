---
UID: NF:cryptxml.CryptXmlEncode
title: CryptXmlEncode function (cryptxml.h)
description: Encodes signature data by using the supplied XML writer callback function.
helpviewer_keywords: ["CryptXmlEncode","CryptXmlEncode function [Security]","cryptxml/CryptXmlEncode","security.cryptxmlencode"]
old-location: security\cryptxmlencode.htm
tech.root: security
ms.assetid: fb0cd00c-f410-486e-8910-41c0463f6a74
ms.date: 12/05/2018
ms.keywords: CryptXmlEncode, CryptXmlEncode function [Security], cryptxml/CryptXmlEncode, security.cryptxmlencode
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
req.lib: Cryptxml.lib
req.dll: Cryptxml.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptXmlEncode
 - cryptxml/CryptXmlEncode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cryptxml.dll
api_name:
 - CryptXmlEncode
---

# CryptXmlEncode function


## -description

The <b>CryptXmlEncode</b> function encodes signature data by using the supplied XML writer callback function.

## -parameters

### -param hCryptXml [in]

The handle of the object to be serialized. The handle can be of <b>Signature</b>, <b>Object</b>, or <b>Reference</b> types.

### -param dwCharset

A value of the <a href="/windows/desktop/api/cryptxml/ne-cryptxml-crypt_xml_charset">CRYPT_XML_CHARSET</a> enumeration that specifies the character set of the encoded XML.

### -param rgProperty [in]

A pointer to an array of <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_property">CRYPT_XML_PROPERTY</a> structures that contain additional properties.

### -param cProperty [in]

A <b>ULONG</b> value that specifies the number of entries in the array pointed to by the <i>rgProperty</i> parameter.

### -param pvCallbackState [in, out]

A pointer to an application defined argument that is passed to the XML writer callback function pointed to by the <i>pfnWrite</i> parameter.

### -param pfnWrite [in]

An XML writer callback function to receive the application defined argument pointed to by the <i>pvCallbackState</i> parameter.

## -returns

If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.