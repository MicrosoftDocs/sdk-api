---
UID: NF:shobjidl.INameSpaceTreeControlDropHandler.OnDropPosition
title: INameSpaceTreeControlDropHandler::OnDropPosition
author: windows-sdk-content
description: Called when the item is being dropped within the same level (within the same parent folder) in the tree.
old-location: shell\INameSpaceTreeControlDropHandler_OnDropPosition.htm
old-project: shell
ms.assetid: 72d14961-85d1-428c-b2de-70c49c91b5b0
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: INameSpaceTreeControlDropHandler interface [Windows Shell],OnDropPosition method, INameSpaceTreeControlDropHandler.OnDropPosition, INameSpaceTreeControlDropHandler::OnDropPosition, OnDropPosition, OnDropPosition method [Windows Shell], OnDropPosition method [Windows Shell],INameSpaceTreeControlDropHandler interface, _shell_INameSpaceTreeControlDropHandler_OnDropPosition, shell.INameSpaceTreeControlDropHandler_OnDropPosition, shobjidl/INameSpaceTreeControlDropHandler::OnDropPosition
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
req.typenames: VPWATERMARKFLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shobjidl.h
api_name:
-	INameSpaceTreeControlDropHandler.OnDropPosition
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# INameSpaceTreeControlDropHandler::OnDropPosition


## -description


Called when the item is being dropped within the same level (within the same parent folder) in the tree.


## -parameters




### -param psiOver [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> interface representing the item underneath the mouse cursor. Optional.


### -param psiaData [in]

Type: <b><a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> array representing a data object.


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



