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

# MS_ADDINFO_BLOB_ structure


## -description


The <b>MS_ADDINFO_BLOB</b> structure provides additional information for in-memory <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a> subject types.


## -struct-fields




### -field cbStruct

The size, in bytes, of this structure.


### -field cbMemObject

The size, in bytes, of the data in the <i>pbMemObject</i> member.


### -field pbMemObject

A pointer to the in-memory BLOB subject.


### -field cbMemSignedMsg

The size, in bytes, of the data in the <i>pbMemSignedMsg</i> member.


### -field pbMemSignedMsg

A pointer to the signed message.

