---
UID: NC:cryptxml.PFN_CRYPT_XML_ENUM_ALG_INFO
title: PFN_CRYPT_XML_ENUM_ALG_INFO
author: windows-sdk-content
description: Enumerates predefined and registered CRYPT_XML_ALGORITHM_INFO entries.
old-location: security\pfn_crypt_xml_enum_alg_info.htm
tech.root: SecCrypto
ms.assetid: d4e4752a-347c-45b0-97f2-6a692088c908
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: PFN_CRYPT_XML_ENUM_ALG_INFO, PFN_CRYPT_XML_ENUM_ALG_INFO callback, PFN_CRYPT_XML_ENUM_ALG_INFO callback function [Security], cryptxml/PFN_CRYPT_XML_ENUM_ALG_INFO, security.pfn_crypt_xml_enum_alg_info
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
 - PFN_CRYPT_XML_ENUM_ALG_INFO
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFN_CRYPT_XML_ENUM_ALG_INFO callback function


## -description


The <i>PFN_CRYPT_XML_ENUM_ALG_INFO</i> callback function enumerates predefined and registered 
 <a href="https://msdn.microsoft.com/ab6ec092-d25d-4ca0-8206-b7e5ad36d69b">CRYPT_XML_ALGORITHM_INFO</a> entries.


## -parameters




### -param *pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/ab6ec092-d25d-4ca0-8206-b7e5ad36d69b">CRYPT_XML_ALGORITHM_INFO</a> structure.


### -param *pvArg [in, out, optional]

A pointer to an argument that is passed to the callback function from the calling function.


## -returns



If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>.




## -remarks



If the callback function returns <b>FALSE</b>, then stop the enumeration.

 This function enumerates  either the predefined and registered 
 entries or the structures identified by a selected URI group.



