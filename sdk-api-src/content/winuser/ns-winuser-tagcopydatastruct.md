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

# tagCOPYDATASTRUCT structure


## -description


Contains data to be passed to another application by the <a href="https://msdn.microsoft.com/d937a260-9fd2-4450-a762-20120f589ab1">WM_COPYDATA</a> message. 


## -struct-fields




### -field dwData

Type: <b>ULONG_PTR</b>

The data to be passed to the receiving application. 


### -field cbData

Type: <b>DWORD</b>

The size, in bytes, of the data pointed to by the <b>lpData</b> member. 


### -field lpData

Type: <b>PVOID</b>

The data to be passed to the receiving application. This member can be <b>NULL</b>. 


## -see-also




<a href="https://msdn.microsoft.com/d937a260-9fd2-4450-a762-20120f589ab1">WM_COPYDATA</a>
 

 

