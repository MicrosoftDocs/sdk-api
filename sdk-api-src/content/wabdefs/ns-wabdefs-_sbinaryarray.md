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

# _SBinaryArray structure


## -description


Do not use. An array of entry identifiers representing MAPI objects. Uses the same implementation as <a href="31fc6e1b-c2c1-4e74-a760-957a60005d1e">SBinaryArray</a>.


## -struct-fields




### -field cValues

Type: <b>ULONG</b>

Variable of type <b>ULONG</b> that specifies the number of entry identifiers.


### -field lpbin

Type: <b><a href="7710f883-e168-4c49-8f29-d18792b80ad4">SBinary</a>*</b>

Array of variables of type <a href="7710f883-e168-4c49-8f29-d18792b80ad4">SBinary</a> that specify the entry identifiers.

