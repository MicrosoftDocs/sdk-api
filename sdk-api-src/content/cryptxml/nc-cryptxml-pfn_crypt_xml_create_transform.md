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

# PFN_CRYPT_XML_CREATE_TRANSFORM callback function


## -description


The  <i>PFN_CRYPT_XML_CREATE_TRANSFORM</i>  callback function creates a transform for a specified data provider.


## -parameters




### -param *pTransform [in]

A <a href="https://msdn.microsoft.com/4eb99c1e-fa06-41ec-906c-a3ba34e7aaeb">CRYPT_XML_ALGORITHM</a> structure that specifies the transform to apply.


### -param *pProviderIn [in]

A pointer to a <a href="https://msdn.microsoft.com/98f32310-a4fa-414c-8a3e-877839eacd1b">CRYPT_XML_DATA_PROVIDER</a> structure that specifies the data provider to use as input for the transform. 


### -param *pProviderOut [out]

A pointer to a  <a href="https://msdn.microsoft.com/98f32310-a4fa-414c-8a3e-877839eacd1b">CRYPT_XML_DATA_PROVIDER</a> structure to receive the data provider of the transform.


## -returns



If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.




## -remarks



In the transform chain, the output of a transform is the input of the next transform in the chain.

 The implementation of the callback function is responsible for calling the  provider close function on the input transform to release the input provider.



