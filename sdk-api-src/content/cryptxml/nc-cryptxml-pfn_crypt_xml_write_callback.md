---
UID: NC:cryptxml.PFN_CRYPT_XML_WRITE_CALLBACK
title: PFN_CRYPT_XML_WRITE_CALLBACK (cryptxml.h)
description: Writes XML data.
helpviewer_keywords: ["PFN_CRYPT_XML_WRITE_CALLBACK","PFN_CRYPT_XML_WRITE_CALLBACK callback","PFN_CRYPT_XML_WRITE_CALLBACK callback function [Security]","cryptxml/PFN_CRYPT_XML_WRITE_CALLBACK","security.pfn_crypt_xml_write_callback"]
old-location: security\pfn_crypt_xml_write_callback.htm
tech.root: security
ms.assetid: 722f6ab4-ca6f-460d-9282-e4b7ca484077
ms.date: 12/05/2018
ms.keywords: PFN_CRYPT_XML_WRITE_CALLBACK, PFN_CRYPT_XML_WRITE_CALLBACK callback, PFN_CRYPT_XML_WRITE_CALLBACK callback function [Security], cryptxml/PFN_CRYPT_XML_WRITE_CALLBACK, security.pfn_crypt_xml_write_callback
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
 - PFN_CRYPT_XML_WRITE_CALLBACK
 - cryptxml/PFN_CRYPT_XML_WRITE_CALLBACK
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
 - PFN_CRYPT_XML_WRITE_CALLBACK
---

# PFN_CRYPT_XML_WRITE_CALLBACK callback function


## -description

The <i>PFN_CRYPT_XML_WRITE_CALLBACK</i> callback function writes XML data.

## -parameters

### -param pvCallbackState [in, out]

A pointer to an argument that is passed to the callback function pointed to by the <i>pfnWrite</i> parameter of the <a href="/windows/desktop/api/cryptxml/nc-cryptxml-cryptxmldllencodealgorithm">CryptXmlDllEncodeAlgorithm</a> function.

### -param pbData [in]

A pointer to a block of data to be written.

### -param cbData

The size, in bytes, of the data pointed to by the <i>pbData</i> parameter.

## -returns

If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.
