---
UID: NF:ocidl.IOleUndoManager.Open
title: IOleUndoManager::Open
author: windows-sdk-content
description: Opens a new parent undo unit, which becomes part of its containing unit's undo stack.
old-location: com\ioleundomanager_open.htm
tech.root: com
ms.assetid: b494d5b9-5def-4249-8b6d-37b26993cc24
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IOleUndoManager interface [COM],Open method, IOleUndoManager.Open, IOleUndoManager::Open, Open, Open method [COM], Open method [COM],IOleUndoManager interface, _ole_ioleundomanager_open, com.ioleundomanager_open, ocidl/IOleUndoManager::Open
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
 - IOleUndoManager.Open
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleUndoManager::Open


## -description


Opens a new parent undo unit, which becomes part of its containing unit's undo stack.


## -parameters




### -param pPUU [in]

An <a href="https://msdn.microsoft.com/4407d673-286a-4221-ae35-09b9865161f8">IOleParentUndoUnit</a> pointer to the parent undo unit to be opened.


## -returns



This method returns S_OK if the parent undo unit was successfully opened or if a currently open unit is blocked. If the undo manager is currently disabled, it will return S_OK and do nothing else.




## -remarks



This method is implemented the same as <a href="https://msdn.microsoft.com/185eae3b-5323-45f1-9810-47bd21ce0d22">IOleParentUndoUnit::Open</a>. The specified parent unit is created and remains open. The undo manager then calls the <a href="https://msdn.microsoft.com/3288e0c6-e345-4c4d-a7bf-0c5f45c19732">IOleUndoManager::Add</a> or <b>IOleUndoManager::Open</b> methods on this parent unit to add new units to it. This parent unit receives any additional undo units until its <a href="https://msdn.microsoft.com/4546f270-5cef-42a3-b07a-f0a491e78849">IOleUndoManager::Close</a> method is called.

The parent unit specified by <i>pPUU</i> is not added to the undo stack until its <a href="https://msdn.microsoft.com/4546f270-5cef-42a3-b07a-f0a491e78849">IOleUndoManager::Close</a> method is called with the <i>fCommit</i> parameter set to <b>TRUE</b>.

The parent undo unit or undo manager must contain any undo unit given to it unless it is blocked. If it is blocked, it must return S_OK but should do nothing else.




## -see-also




<a href="https://msdn.microsoft.com/4407d673-286a-4221-ae35-09b9865161f8">IOleParentUndoUnit</a>



<a href="https://msdn.microsoft.com/0f507506-3589-4d5b-b1b3-010bce9ae42f">IOleUndoManager</a>
 

 

