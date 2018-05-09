---
UID: NF:shobjidl.INameSpaceTreeControlDropHandler.OnDragEnter
title: INameSpaceTreeControlDropHandler::OnDragEnter
author: windows-driver-content
description: Called on drag enter to set drag effect, as specified.
old-location: shell\INameSpaceTreeControlDropHandler_OnDragEnter.htm
old-project: shell
ms.assetid: b9a87024-d62e-4006-a716-c1461d9c9ffe
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: INameSpaceTreeControlDropHandler interface [Windows Shell],OnDragEnter method, INameSpaceTreeControlDropHandler.OnDragEnter, INameSpaceTreeControlDropHandler::OnDragEnter, OnDragEnter, OnDragEnter method [Windows Shell], OnDragEnter method [Windows Shell],INameSpaceTreeControlDropHandler interface, _shell_INameSpaceTreeControlDropHandler_OnDragEnter, shell.INameSpaceTreeControlDropHandler_OnDragEnter, shobjidl/INameSpaceTreeControlDropHandler::OnDragEnter
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: VPWATERMARKFLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shobjidl.h
api_name:
-	INameSpaceTreeControlDropHandler.OnDragEnter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# INameSpaceTreeControlDropHandler::OnDragEnter


## -description


Called on drag enter to set drag effect, as specified.


## -parameters




### -param psiOver [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> interface representing the item underneath the mouse cursor. Optional.


### -param psiaData [in]

Type: <b><a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> array containing the items being dragged.


### -param fOutsideSource [in]

Type: <b>BOOL</b>

Specifies whether drag started outside target area.


### -param grfKeyState [in]

Type: <b>DWORD</b>

The current state of keyboard modifier keys.


### -param pdwEffect [in, out]

Type: <b>DWORD*</b>

On success, contains a pointer to the drag effect value.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Failing this method blocks the drag operation in the namespace tree control (NSTC).




## -see-also




<a href="https://msdn.microsoft.com/2e4d7013-910c-4a6e-8eee-818e1f2302ac">IDropTarget::DragEnter</a>



<a href="https://msdn.microsoft.com/5d2c1783-daeb-488d-93b9-34df2712d849">INameSpaceTreeControlDropHandler</a>
 

 

