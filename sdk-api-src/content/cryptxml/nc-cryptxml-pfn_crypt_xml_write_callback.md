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

# PFN_CRYPT_XML_WRITE_CALLBACK callback function


## -description


The <i>PFN_CRYPT_XML_WRITE_CALLBACK</i> callback function writes XML data.


## -parameters




### -param *pvCallbackState [in, out]

A pointer to an argument that is passed to the callback function pointed to by the <i>pfnWrite</i> parameter of the <a href="https://msdn.microsoft.com/ef21897e-66f1-436c-8440-91422f5c95a7">CryptXmlDllEncodeAlgorithm</a> function.


### -param *pbData [in]

A pointer to a block of data to be written.


### -param cbData

The size, in bytes, of the data pointed to by the <i>pbData</i> parameter.


## -returns



If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.



