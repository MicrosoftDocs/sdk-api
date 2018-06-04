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

# _SPC_INDIRECT_DATA_CONTENT structure


## -description


The <b>SPC_INDIRECT_DATA_CONTENT</b> structure is used in Authenticode signatures to store the digest and other attributes of the signed file.


## -struct-fields




### -field Data

A <a href="https://msdn.microsoft.com/84057581-d0a9-464a-9399-ba806e37516f">CRYPT_ATTRIBUTE_TYPE_VALUE</a> that contains attributes of the digested file.


### -field DigestAlgorithm

Specifies the digest algorithm used to hash the file.


### -field Digest

The Authenticode digest value of the file using the algorithm specified in the  <i>DigestAlgorithm</i> parameter.

