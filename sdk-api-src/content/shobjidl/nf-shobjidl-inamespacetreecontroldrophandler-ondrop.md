---
UID: NF:shobjidl.INameSpaceTreeControlDropHandler.OnDrop
title: INameSpaceTreeControlDropHandler::OnDrop (shobjidl.h)
author: windows-sdk-content
description: Called on drop to set drop effect, as specified.
old-location: shell\INameSpaceTreeControlDropHandler_OnDrop.htm
tech.root: shell
ms.assetid: 05c677fb-a2e2-4aa5-bb27-4dc437ca408c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControlDropHandler interface [Windows Shell],OnDrop method, INameSpaceTreeControlDropHandler.OnDrop, INameSpaceTreeControlDropHandler::OnDrop, OnDrop, OnDrop method [Windows Shell], OnDrop method [Windows Shell],INameSpaceTreeControlDropHandler interface, _shell_INameSpaceTreeControlDropHandler_OnDrop, shell.INameSpaceTreeControlDropHandler_OnDrop, shobjidl/INameSpaceTreeControlDropHandler::OnDrop
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
 - INameSpaceTreeControlDropHandler.OnDrop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INameSpaceTreeControlDropHandler::OnDrop


## -description


Called on drop to set drop effect, as specified.


## -parameters




### -param psiOver [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> interface representing the item underneath the mouse cursor. Optional.


### -param psiaData [in]

Type: <b><a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> array representing a data object.


### -param iPosition [in]

Type: <b>int</b>

Specifies drop position.


### -param grfKeyState [in]

Type: <b>DWORD</b>

The current state of keyboard modifier keys.


### -param pdwEffect [in, out]

Type: <b>DWORD*</b>

A pointer to the drop effect value.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<div class="alert"><b>Note</b>  To overwrite the default drop behavior, a client should fail this method; success proceeds with the default drop operation.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/7ea6d815-bf8f-47d5-99d3-f9a55bafee2e">IDropTarget::Drop</a>



<a href="https://msdn.microsoft.com/5d2c1783-daeb-488d-93b9-34df2712d849">INameSpaceTreeControlDropHandler</a>
 

 

