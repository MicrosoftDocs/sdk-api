---
UID: NF:cryptxml.CryptXmlGetTransforms
title: CryptXmlGetTransforms function
author: windows-sdk-content
description: Returns information about the default transform chain engine.
old-location: security\cryptxmlgettransforms.htm
old-project: SecCrypto
ms.assetid: 676f5216-70bd-455d-9e08-230b2599e166
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: CryptXmlGetTransforms, CryptXmlGetTransforms function [Security], cryptxml/CryptXmlGetTransforms, security.cryptxmlgettransforms
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: CRYPT_XML_PROPERTY_ID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cryptxml.dll
api_name:
 - CryptXmlGetTransforms
product: Windows
targetos: Windows
req.lib: Cryptxml.lib
req.dll: Cryptxml.dll
req.irql: 
---

# CryptXmlGetTransforms function


## -description


The <b>CryptXmlGetTransforms</b> function returns information about the default transform chain engine.


## -parameters




### -param ppConfig

TBD




#### - pConfig [out]

A pointer to a pointer to a <a href="https://msdn.microsoft.com/ad18ee99-685d-4a79-bd91-492df20edb8c">CRYPT_XML_TRANSFORM_CHAIN_CONFIG</a> structure to receive the returned transform information.


## -returns



If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.



