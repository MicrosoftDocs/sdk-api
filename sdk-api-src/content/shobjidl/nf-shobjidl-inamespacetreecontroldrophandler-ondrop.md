---
UID: NF:shobjidl.INameSpaceTreeControlDropHandler.OnDrop
title: INameSpaceTreeControlDropHandler::OnDrop method
author: windows-driver-content
description: Called on drop to set drop effect, as specified.
old-location: shell\INameSpaceTreeControlDropHandler_OnDrop.htm
old-project: shell
ms.assetid: 05c677fb-a2e2-4aa5-bb27-4dc437ca408c
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: INameSpaceTreeControlDropHandler, INameSpaceTreeControlDropHandler interface [Windows Shell], OnDrop method, INameSpaceTreeControlDropHandler::OnDrop, OnDrop method [Windows Shell], OnDrop method [Windows Shell], INameSpaceTreeControlDropHandler interface, OnDrop,INameSpaceTreeControlDropHandler.OnDrop, _shell_INameSpaceTreeControlDropHandler_OnDrop, shell.INameSpaceTreeControlDropHandler_OnDrop, shobjidl/INameSpaceTreeControlDropHandler::OnDrop
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
-	INameSpaceTreeControlDropHandler.OnDrop
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# INameSpaceTreeControlDropHandler::OnDrop method


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
 

 

