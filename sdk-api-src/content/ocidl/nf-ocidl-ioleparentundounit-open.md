---
UID: NF:ocidl.IOleParentUndoUnit.Open
title: IOleParentUndoUnit::Open
author: windows-sdk-content
description: Opens a new parent undo unit, which becomes part of the containing unit's undo stack.
old-location: com\ioleparentundounit_open.htm
tech.root: com
ms.assetid: 185eae3b-5323-45f1-9810-47bd21ce0d22
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IOleParentUndoUnit interface [COM],Open method, IOleParentUndoUnit.Open, IOleParentUndoUnit::Open, Open, Open method [COM], Open method [COM],IOleParentUndoUnit interface, _ole_ioleparentundounit_open, com.ioleparentundounit_open, ocidl/IOleParentUndoUnit::Open
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
 - IOleParentUndoUnit.Open
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleParentUndoUnit::Open


## -description


Opens a new parent undo unit, which becomes part of the containing unit's undo stack.


## -parameters




### -param pPUU [in]

An <a href="https://msdn.microsoft.com/4407d673-286a-4221-ae35-09b9865161f8">IOleParentUndoUnit</a> pointer to the parent undo unit to be opened.


## -returns



This method returns S_OK if the parent undo unit was successfully opened or it is currently blocked.




## -remarks



The specified parent unit is created and remains open. The undo manager then calls the <a href="https://msdn.microsoft.com/86db3308-6f01-47f1-ba28-3ed5e70b7cb9">IOleParentUndoUnit::Add</a> or <b>IOleParentUndoUnit::Open</b> methods on this parent unit to add new units to it. This parent unit receives any additional undo units until its <a href="https://msdn.microsoft.com/dcfe1962-c40f-4d3f-ae6a-b70755adebe8">IOleParentUndoUnit::Close</a> method is called.

The parent unit specified by <i>pPUU</i> is not added to the undo stack until its <a href="https://msdn.microsoft.com/dcfe1962-c40f-4d3f-ae6a-b70755adebe8">IOleParentUndoUnit::Close</a> method is called with the <i>fCommit</i> parameter set to <b>TRUE</b>.

The parent undo unit or undo manager must contain any undo unit given to it unless it is blocked. If it is blocked, it must return S_OK but should do nothing else.




## -see-also




<a href="https://msdn.microsoft.com/4407d673-286a-4221-ae35-09b9865161f8">IOleParentUndoUnit</a>



<a href="https://msdn.microsoft.com/185eae3b-5323-45f1-9810-47bd21ce0d22">IOleParentUndoUnit::Open</a>
 

 

