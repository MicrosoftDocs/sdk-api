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

# ILCombine function


## -description


Combines two <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structures.


## -parameters




### -param pidl1 [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

A pointer to the first <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure.


### -param pidl2 [in]

Type: <b>PCUIDLIST_RELATIVE</b>

A pointer to the second <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure. This structure is appended to the structure pointed to by <i>pidl1</i>.


## -returns



Type: <b>PIDLIST_ABSOLUTE</b>

Returns an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> containing the combined structures. If you set either <i>pidl1</i> or <i>pidl2</i> to <b>NULL</b>, the returned <b>ITEMIDLIST</b> structure is a clone of the non-<b>NULL</b> parameter. Returns <b>NULL</b> if <i>pidl1</i> and <i>pidl2</i> are both set to <b>NULL</b>.



