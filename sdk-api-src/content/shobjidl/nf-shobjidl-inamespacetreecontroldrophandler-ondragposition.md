---
UID: NF:shobjidl.INameSpaceTreeControlDropHandler.OnDragPosition
title: INameSpaceTreeControlDropHandler::OnDragPosition (shobjidl.h)
description: Called when the item is being dragged within the same level (within the same parent folder) in the tree.
old-location: shell\INameSpaceTreeControlDropHandler_OnDragPosition.htm
tech.root: shell
ms.assetid: b3f49da1-81a0-4d54-a2c3-5cb76f8a02de
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControlDropHandler interface [Windows Shell],OnDragPosition method, INameSpaceTreeControlDropHandler.OnDragPosition, INameSpaceTreeControlDropHandler::OnDragPosition, OnDragPosition, OnDragPosition method [Windows Shell], OnDragPosition method [Windows Shell],INameSpaceTreeControlDropHandler interface, _shell_INameSpaceTreeControlDropHandler_OnDragPosition, shell.INameSpaceTreeControlDropHandler_OnDragPosition, shobjidl/INameSpaceTreeControlDropHandler::OnDragPosition
ms.topic: method
f1_keywords:
- shobjidl/INameSpaceTreeControlDropHandler.OnDragPosition
dev_langs:
- c++
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
- Shobjidl.h
api_name:
- INameSpaceTreeControlDropHandler.OnDragPosition
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INameSpaceTreeControlDropHandler::OnDragPosition


## -description


Called when the item is being dragged within the same level (within the same parent folder) in the tree.


## -parameters




### -param psiOver [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> interface representing the item underneath the mouse cursor. Optional.


### -param psiaData [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>*</b>

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> array containing the items being dragged.


### -param iNewPosition [in]

Type: <b>int</b>

The index if the item being dragged is between items; otherwise, NSTCDHPOS_ONTOP (-1).


### -param iOldPosition [in]

Type: <b>int</b>

The old position.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Failing this method prevents the item rearrangment.



