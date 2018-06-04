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

# _CRYPT_XML_DATA_PROVIDER structure


## -description


The <b>CRYPT_XML_DATA_PROVIDER</b> structure specifies the interface to the XML data provider.


## -struct-fields




### -field pvCallbackState

An application-defined argument that is passed to
    the <b>pfnRead</b> and <b>pfnClose</b> callback functions.


### -field cbBufferSize

 The size, in bytes, of the data provider's buffer. The size can be zero if the size does not matter or if the size cannot be determined by the provider.
    This value is used by a caller of <b>pfnRead</b> to determine the necessary size of the receiving buffer.


### -field pfnRead

A pointer to a <a href="https://msdn.microsoft.com/86c7003e-eee2-4adf-adf4-8f9d1acb5c45">PFN_CRYPT_XML_DATA_PROVIDER_READ</a> callback function used to read data.


### -field pfnClose

A pointer to a <a href="https://msdn.microsoft.com/886fbe92-f9ab-49d4-968a-afeadbf2f030">PFN_CRYPT_XML_DATA_PROVIDER_CLOSE</a> callback function used to release the data provider. When you have finished using the data provider, you must release it.

