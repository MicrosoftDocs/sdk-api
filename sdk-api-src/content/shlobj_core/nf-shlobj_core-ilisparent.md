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

# ILIsParent function


## -description


Tests whether an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure is the parent of another <b>ITEMIDLIST</b> structure.


## -parameters




### -param pidl1 [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

A pointer to an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> (PIDL) structure that specifies the parent. This must be an absolute PIDL.


### -param pidl2 [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

A pointer to an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> (PIDL) structure that specifies the child. This must be an absolute PIDL.


### -param fImmediate [in]

Type: <b>BOOL</b>

A Boolean value that is set to <b>TRUE</b> to test for immediate parents of <i>pidl2</i>, or <b>FALSE</b> to test for any parents of <i>pidl2</i>.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if <i>pidl1</i> is a parent of <i>pidl2</i>. If <i>fImmediate</i> is set to <b>TRUE</b>, the function only returns <b>TRUE</b> if <i>pidl1</i> is the immediate parent of <i>pidl2</i>. Otherwise, the function returns <b>FALSE</b>.



