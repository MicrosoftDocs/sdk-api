---
UID: NC:cryptxml.CryptXmlDllEncodeKeyValue
title: CryptXmlDllEncodeKeyValue
author: windows-driver-content
description: Encodes a KeyValue element.
old-location: security\cryptxmldllencodekeyvalue.htm
old-project: SecCrypto
ms.assetid: a0737139-a820-455d-85f4-c56b63a1a8e0
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: CryptXmlDllEncodeKeyValue, CryptXmlDllEncodeKeyValue function pointer [Security], cryptxml/CryptXmlDllEncodeKeyValue, security.cryptxmldllencodekeyvalue
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: CRYPTUI_WIZ_IMPORT_SRC_INFO, *PCRYPTUI_WIZ_IMPORT_SRC_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	cryptxml.h
api_name:
-	CryptXmlDllEncodeKeyValue
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# CryptXmlDllEncodeKeyValue callback


## -description


The <b>CryptXmlDllEncodeKeyValue</b> function encodes a <b>KeyValue</b> element.


## -parameters




### -param hKey [in]

The handle of the key value to encode.


### -param dwCharset

A value of the <a href="https://msdn.microsoft.com/3f115ac1-a8ed-4151-b3f3-7ddb695802a0">CRYPT_XML_CHARSET</a> enumeration that specifies the character set of the encoded XML.


### -param *pvCallbackState [in, out]

A pointer to an argument that is passed to the callback function pointed to by the <i>pfnWrite</i> parameter.


### -param pfnWrite [in]

An application defined callback function that receives the encoded XML.


## -returns



If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.



