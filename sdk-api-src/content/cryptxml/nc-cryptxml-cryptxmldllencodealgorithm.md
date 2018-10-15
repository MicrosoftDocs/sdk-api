---
UID: NC:cryptxml.CryptXmlDllEncodeAlgorithm
title: CryptXmlDllEncodeAlgorithm
author: windows-sdk-content
description: Encodes SignatureMethod or DigestMethod elements for agile algorithms with default parameters.
old-location: security\cryptxmldllencodealgorithm.htm
tech.root: seccrypto
ms.assetid: ef21897e-66f1-436c-8440-91422f5c95a7
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: CryptXmlDllEncodeAlgorithm, CryptXmlDllEncodeAlgorithm callback, CryptXmlDllEncodeAlgorithm callback function [Security], cryptxml/CryptXmlDllEncodeAlgorithm, security.cryptxmldllencodealgorithm
ms.prod: windows
ms.technology: windows-sdk
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
 - Cryptxml.h
api_name:
 - CryptXmlDllEncodeAlgorithm
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptXmlDllEncodeAlgorithm callback function


## -description


The <b>CryptXmlDllEncodeAlgorithm</b> function encodes <b>SignatureMethod</b> or <b>DigestMethod</b> elements  for agile algorithms with default parameters.

The <b>CryptXmlDllEncodeAlgorithm</b> function is exposed through the exported <a href="https://msdn.microsoft.com/a547e869-3c9f-4408-9895-29fae0cc6066">CryptXmlDllGetInterface</a>  function.


## -parameters




### -param *pAlgInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/ab6ec092-d25d-4ca0-8206-b7e5ad36d69b">CRYPT_XML_ALGORITHM_INFO</a> structure. 


### -param dwCharset

A <a href="https://msdn.microsoft.com/3f115ac1-a8ed-4151-b3f3-7ddb695802a0">CRYPT_XML_CHARSET</a> value that specifies the character set of the encoded XML.


### -param *pvCallbackState [in, out]

A pointer to an argument that is passed to the callback function pointed to by the <i>pfnWrite</i> parameter.


### -param pfnWrite [in]

A <a href="https://msdn.microsoft.com/722f6ab4-ca6f-460d-9282-e4b7ca484077">PFN_CRYPT_XML_WRITE_CALLBACK</a> callback function that receives the encoded XML.


## -returns



If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.



