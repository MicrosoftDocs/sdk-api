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

# EngUnmapFile function


## -description


The <b>EngUnmapFile</b> function unmaps the view of a file from <a href="https://msdn.microsoft.com/5f6fec1a-1134-4765-81be-9b50939e5e66">system space</a>.


## -parameters




### -param iFile [in]

Pointer to the identifier of the mapped file. This identifier was obtained in a prior call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff564971">EngMapFile</a>.


## -returns



<b>EngUnmapFile</b> returns <b>TRUE</b> upon success. Otherwise, it returns <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564971">EngMapFile</a>
 

 

