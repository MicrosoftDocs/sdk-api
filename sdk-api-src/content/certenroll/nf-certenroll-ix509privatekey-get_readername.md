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

# IX509PrivateKey::get_ReaderName


## -description


The <b>ReaderName</b> property specifies or retrieves the name of a smart card reader.

This property is read/write.


## -parameters


## -remarks



If you set this property before opening a key, the reader name is concatenated to the name of the key container. The format is \\.\<i>Reader_Name</i>\<i>Container_Name</i>. Prepending the reader name to the key container name enables the name to be disambiguated in subsequent calls to a cryptographic provider. The private key is typically stored in the smart card key container when a smart card is used.




## -see-also




<a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a>
 

 

