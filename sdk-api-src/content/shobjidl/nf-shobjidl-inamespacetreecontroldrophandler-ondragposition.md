---
UID: NF:shobjidl.INameSpaceTreeControlDropHandler.OnDragPosition
title: INameSpaceTreeControlDropHandler::OnDragPosition
author: windows-sdk-content
description: Called when the item is being dragged within the same level (within the same parent folder) in the tree.
old-location: shell\INameSpaceTreeControlDropHandler_OnDragPosition.htm
old-project: shell
ms.assetid: b3f49da1-81a0-4d54-a2c3-5cb76f8a02de
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: INameSpaceTreeControlDropHandler interface [Windows Shell],OnDragPosition method, INameSpaceTreeControlDropHandler.OnDragPosition, INameSpaceTreeControlDropHandler::OnDragPosition, OnDragPosition, OnDragPosition method [Windows Shell], OnDragPosition method [Windows Shell],INameSpaceTreeControlDropHandler interface, _shell_INameSpaceTreeControlDropHandler_OnDragPosition, shell.INameSpaceTreeControlDropHandler_OnDragPosition, shobjidl/INameSpaceTreeControlDropHandler::OnDragPosition
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: VPWATERMARKFLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - INameSpaceTreeControlDropHandler.OnDragPosition
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# INameSpaceTreeControlDropHandler::OnDragPosition


## -description


Called when the item is being dragged within the same level (within the same parent folder) in the tree.


## -parameters




### -param psiOver [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> interface representing the item underneath the mouse cursor. Optional.


### -param psiaData [in]

Type: <b><a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> array containing the items being dragged.


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



