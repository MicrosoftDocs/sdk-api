---
UID: NF:shobjidl.INameSpaceTreeControlDropHandler.OnDropPosition
title: INameSpaceTreeControlDropHandler::OnDropPosition (shobjidl.h)
description: Called when the item is being dropped within the same level (within the same parent folder) in the tree.
helpviewer_keywords: ["INameSpaceTreeControlDropHandler interface [Windows Shell]","OnDropPosition method","INameSpaceTreeControlDropHandler.OnDropPosition","INameSpaceTreeControlDropHandler::OnDropPosition","OnDropPosition","OnDropPosition method [Windows Shell]","OnDropPosition method [Windows Shell]","INameSpaceTreeControlDropHandler interface","_shell_INameSpaceTreeControlDropHandler_OnDropPosition","shell.INameSpaceTreeControlDropHandler_OnDropPosition","shobjidl/INameSpaceTreeControlDropHandler::OnDropPosition"]
old-location: shell\INameSpaceTreeControlDropHandler_OnDropPosition.htm
tech.root: shell
ms.assetid: 72d14961-85d1-428c-b2de-70c49c91b5b0
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControlDropHandler interface [Windows Shell],OnDropPosition method, INameSpaceTreeControlDropHandler.OnDropPosition, INameSpaceTreeControlDropHandler::OnDropPosition, OnDropPosition, OnDropPosition method [Windows Shell], OnDropPosition method [Windows Shell],INameSpaceTreeControlDropHandler interface, _shell_INameSpaceTreeControlDropHandler_OnDropPosition, shell.INameSpaceTreeControlDropHandler_OnDropPosition, shobjidl/INameSpaceTreeControlDropHandler::OnDropPosition
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INameSpaceTreeControlDropHandler::OnDropPosition
 - shobjidl/INameSpaceTreeControlDropHandler::OnDropPosition
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - INameSpaceTreeControlDropHandler.OnDropPosition
---

# INameSpaceTreeControlDropHandler::OnDropPosition


## -description

Called when the item is being dropped within the same level (within the same parent folder) in the tree.

## -parameters

### -param psiOver [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> interface representing the item underneath the mouse cursor. Optional.

### -param psiaData [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>*</b>

A pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> array representing a data object.

### -param iNewPosition [in]

Type: <b>int</b>

The index if the item being dropped is between items; otherwise, NSTCDHPOS_ONTOP (-1).

### -param iOldPosition [in]

Type: <b>int</b>

Specifies old position.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.

## -remarks

Failing this method prevents the item rearrangment from happening.