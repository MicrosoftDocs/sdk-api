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

# UiaFindParams structure


## -description


<div class="alert"><b>Note</b>  This structure is deprecated.</div><div> </div>  Contains parameters used in the <a href="https://msdn.microsoft.com/fe86b393-9c8d-46f1-85dc-5ac37f423ce0">UiaFind</a> function.


## -struct-fields




### -field MaxDepth

Type: <b>int</b>

The maximum depth to which to search the tree for matching elements.


### -field FindFirst

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> to return only the first matching element; <b>FALSE</b> to return all matching elements.


### -field ExcludeRoot

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> to exclude the root element; otherwise <b>FALSE</b>.


### -field pFindCondition

Type: <b><a href="https://msdn.microsoft.com/82b5db01-08c9-4518-9d33-15d7813d0c80">UiaCondition</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/82b5db01-08c9-4518-9d33-15d7813d0c80">UiaCondition</a> structure that contains information about a condition that returned elements must match.

