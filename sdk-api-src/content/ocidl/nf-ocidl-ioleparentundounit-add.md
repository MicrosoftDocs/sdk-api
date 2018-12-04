---
UID: NF:ocidl.IOleParentUndoUnit.Add
title: IOleParentUndoUnit::Add
author: windows-sdk-content
description: Adds a simple undo unit to the collection.
old-location: com\ioleparentundounit_add.htm
tech.root: com
ms.assetid: 86db3308-6f01-47f1-ba28-3ed5e70b7cb9
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: Add, Add method [COM], Add method [COM],IOleParentUndoUnit interface, IOleParentUndoUnit interface [COM],Add method, IOleParentUndoUnit.Add, IOleParentUndoUnit::Add, _ole_ioleparentundounit_add, com.ioleparentundounit_add, ocidl/IOleParentUndoUnit::Add
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IOleParentUndoUnit.Add
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleParentUndoUnit::Add


## -description


Adds a simple undo unit to the collection.


## -parameters




### -param pUU [in]

An <a href="https://msdn.microsoft.com/0822c894-b96c-4b69-94d2-b052dff81f6e">IOleUndoUnit</a> pointer to the undo unit to be added.


## -returns



This method returns S_OK if the specified unit was successfully added or the parent unit was blocked.




## -remarks



The parent undo unit or undo manager must accept any undo unit given to it, unless it is blocked. If it is blocked, it should do nothing but return S_OK.




## -see-also




<a href="https://msdn.microsoft.com/4407d673-286a-4221-ae35-09b9865161f8">IOleParentUndoUnit</a>



<a href="https://msdn.microsoft.com/3288e0c6-e345-4c4d-a7bf-0c5f45c19732">IOleUndoManager::Add</a>
 

 

