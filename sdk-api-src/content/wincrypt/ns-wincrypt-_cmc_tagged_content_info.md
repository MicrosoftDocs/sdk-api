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

# _CMC_TAGGED_CONTENT_INFO structure


## -description


The <b>CMC_TAGGED_CONTENT_INFO</b> structure is used in the 
<a href="https://msdn.microsoft.com/6245af5a-7a19-4665-bf6c-ad803998d840">CMC_DATA_INFO</a> and 
<a href="https://msdn.microsoft.com/82d9314f-2f0f-4a98-a0da-a89cd8905886">CMC_RESPONSE_INFO</a> structures.


## -struct-fields




### -field dwBodyPartID

<b>DWORD</b> identifying the tagged other message.


### -field EncodedContentInfo

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DER_BLOB</a> structure that contains the encoded content information.

