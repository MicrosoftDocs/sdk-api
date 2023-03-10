---
UID: NC:cryptxml.CryptXmlDllEncodeAlgorithm
title: CryptXmlDllEncodeAlgorithm (cryptxml.h)
description: Encodes SignatureMethod or DigestMethod elements for agile algorithms with default parameters.
helpviewer_keywords: ["CryptXmlDllEncodeAlgorithm","CryptXmlDllEncodeAlgorithm callback","CryptXmlDllEncodeAlgorithm callback function [Security]","cryptxml/CryptXmlDllEncodeAlgorithm","security.cryptxmldllencodealgorithm"]
old-location: security\cryptxmldllencodealgorithm.htm
tech.root: security
ms.assetid: ef21897e-66f1-436c-8440-91422f5c95a7
ms.date: 12/05/2018
ms.keywords: CryptXmlDllEncodeAlgorithm, CryptXmlDllEncodeAlgorithm callback, CryptXmlDllEncodeAlgorithm callback function [Security], cryptxml/CryptXmlDllEncodeAlgorithm, security.cryptxmldllencodealgorithm
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptXmlDllEncodeAlgorithm
 - cryptxml/CryptXmlDllEncodeAlgorithm
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Cryptxml.h
api_name:
 - CryptXmlDllEncodeAlgorithm
---

# CryptXmlDllEncodeAlgorithm callback function


## -description

The <b>CryptXmlDllEncodeAlgorithm</b> function encodes <b>SignatureMethod</b> or <b>DigestMethod</b> elements  for agile algorithms with default parameters.

The <b>CryptXmlDllEncodeAlgorithm</b> function is exposed through the exported <a href="/windows/desktop/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface">CryptXmlDllGetInterface</a>  function.

## -parameters

### -param pAlgInfo [in]

A pointer to a <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_algorithm_info">CRYPT_XML_ALGORITHM_INFO</a> structure.

### -param dwCharset

A <a href="/windows/desktop/api/cryptxml/ne-cryptxml-crypt_xml_charset">CRYPT_XML_CHARSET</a> value that specifies the character set of the encoded XML.

### -param pvCallbackState [in, out]

A pointer to an argument that is passed to the callback function pointed to by the <i>pfnWrite</i> parameter.

### -param pfnWrite [in]

A <a href="/windows/desktop/api/cryptxml/nc-cryptxml-pfn_crypt_xml_write_callback">PFN_CRYPT_XML_WRITE_CALLBACK</a> callback function that receives the encoded XML.

## -returns

If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.
