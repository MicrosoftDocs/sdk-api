---
UID: NC:cryptxml.CryptXmlDllEncodeKeyValue
title: CryptXmlDllEncodeKeyValue (cryptxml.h)
author: windows-sdk-content
description: Encodes a KeyValue element.
old-location: security\cryptxmldllencodekeyvalue.htm
tech.root: SecCrypto
ms.assetid: a0737139-a820-455d-85f4-c56b63a1a8e0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CryptXmlDllEncodeKeyValue, CryptXmlDllEncodeKeyValue callback, CryptXmlDllEncodeKeyValue callback function [Security], cryptxml/CryptXmlDllEncodeKeyValue, security.cryptxmldllencodekeyvalue
ms.topic: callback
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
 - UserDefined
api_location:
 - cryptxml.h
api_name:
 - CryptXmlDllEncodeKeyValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CryptXmlDllEncodeKeyValue callback function


## -description


The <b>CryptXmlDllEncodeKeyValue</b> function encodes a <b>KeyValue</b> element.


## -parameters




### -param hKey [in]

The handle of the key value to encode.


### -param dwCharset

A value of the <a href="https://docs.microsoft.com/windows/desktop/api/cryptxml/ne-cryptxml-crypt_xml_charset">CRYPT_XML_CHARSET</a> enumeration that specifies the character set of the encoded XML.


### -param *pvCallbackState [in, out]

A pointer to an argument that is passed to the callback function pointed to by the <i>pfnWrite</i> parameter.


### -param pfnWrite [in]

An application defined callback function that receives the encoded XML.


## -returns



If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.



