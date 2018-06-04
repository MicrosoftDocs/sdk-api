---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



