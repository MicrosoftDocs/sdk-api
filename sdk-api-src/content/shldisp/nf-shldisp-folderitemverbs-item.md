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

# FolderItemVerbs::Item


## -description


Retrieves the <a href="https://msdn.microsoft.com/22f52e3f-875e-4dde-8875-3228639bc7f1">FolderItemVerb</a> object for a specified item in the collection.


## -parameters




### -param index




### -param ppid






#### - iIndex [in]

Type: <b>Variant</b>

The zero-based index of the item to retrieve. This value must be less than the value of the <a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a> property.


## -returns



Type: <b><a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>**</b>

Object that receives the <a href="https://msdn.microsoft.com/22f52e3f-875e-4dde-8875-3228639bc7f1">FolderItemVerb</a> object.



