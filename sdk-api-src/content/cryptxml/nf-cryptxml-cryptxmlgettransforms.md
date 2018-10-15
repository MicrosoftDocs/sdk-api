---
UID: NF:cryptxml.CryptXmlGetTransforms
title: CryptXmlGetTransforms function
author: windows-sdk-content
description: Returns information about the default transform chain engine.
old-location: security\cryptxmlgettransforms.htm
tech.root: seccrypto
ms.assetid: 676f5216-70bd-455d-9e08-230b2599e166
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: CryptXmlGetTransforms, CryptXmlGetTransforms function [Security], cryptxml/CryptXmlGetTransforms, security.cryptxmlgettransforms
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Cryptxml.lib
req.dll: Cryptxml.dll
req.irql: 
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
req.typenames: 
req.redist: 
---

# CryptXmlGetTransforms function


## -description


The <b>CryptXmlGetTransforms</b> function returns information about the default transform chain engine.


## -parameters




### -param ppConfig [out]

A pointer to a pointer to a <a href="https://msdn.microsoft.com/en-us/library/Dd433867(v=VS.85).aspx">CRYPT_XML_TRANSFORM_CHAIN_CONFIG</a> structure to receive the returned transform information.


## -returns



If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.



