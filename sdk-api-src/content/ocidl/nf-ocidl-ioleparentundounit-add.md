---
UID: NF:ocidl.IOleParentUndoUnit.Add
title: IOleParentUndoUnit::Add (ocidl.h)
description: Adds a simple undo unit to the collection.
helpviewer_keywords: ["Add","Add method [COM]","Add method [COM]","IOleParentUndoUnit interface","IOleParentUndoUnit interface [COM]","Add method","IOleParentUndoUnit.Add","IOleParentUndoUnit::Add","_ole_ioleparentundounit_add","com.ioleparentundounit_add","ocidl/IOleParentUndoUnit::Add"]
old-location: com\ioleparentundounit_add.htm
tech.root: com
ms.assetid: 86db3308-6f01-47f1-ba28-3ed5e70b7cb9
ms.date: 12/05/2018
ms.keywords: Add, Add method [COM], Add method [COM],IOleParentUndoUnit interface, IOleParentUndoUnit interface [COM],Add method, IOleParentUndoUnit.Add, IOleParentUndoUnit::Add, _ole_ioleparentundounit_add, com.ioleparentundounit_add, ocidl/IOleParentUndoUnit::Add
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOleParentUndoUnit::Add
 - ocidl/IOleParentUndoUnit::Add
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IOleParentUndoUnit.Add
---

# IOleParentUndoUnit::Add


## -description

Adds a simple undo unit to the collection.

## -parameters

### -param pUU [in]

An <a href="/windows/desktop/api/ocidl/nn-ocidl-ioleundounit">IOleUndoUnit</a> pointer to the undo unit to be added.

## -returns

This method returns S_OK if the specified unit was successfully added or the parent unit was blocked.

## -remarks

The parent undo unit or undo manager must accept any undo unit given to it, unless it is blocked. If it is blocked, it should do nothing but return S_OK.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleparentundounit">IOleParentUndoUnit</a>



<a href="/windows/desktop/api/ocidl/nf-ocidl-ioleundomanager-add">IOleUndoManager::Add</a>