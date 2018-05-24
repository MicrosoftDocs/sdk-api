---
UID: NF:shobjidl_core.IRegTreeItem.SetCheckState
title: IRegTreeItem::SetCheckState
author: windows-driver-content
description: Sets the state of a check box item in a tree-view control.
old-location: shell\IRegTreeItem_SetCheckState.htm
old-project: shell
ms.assetid: 0ba25491-8d18-4040-a256-9078b91e4f3f
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: FALSE, IRegTreeItem interface [Windows Shell],SetCheckState method, IRegTreeItem.SetCheckState, IRegTreeItem::SetCheckState, SetCheckState, SetCheckState method [Windows Shell], SetCheckState method [Windows Shell],IRegTreeItem interface, TRUE, _win32_IRegTreeItem_SetCheckState, shell.IRegTreeItem_SetCheckState, shobjidl_core/IRegTreeItem::SetCheckState
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	IRegTreeItem.SetCheckState
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IRegTreeItem::SetCheckState


## -description


Sets the state of a check box item in a tree-view control.


## -parameters




### -param bCheck [in]

Type: <b>BOOL</b>


          A <b>BOOL</b> that sets the state of the check box.
        



#### TRUE

The check box is checked.



#### FALSE

The check box is not checked.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/a9ae0fb3-4a6e-473e-9fa3-d3894834fb72">IRegTreeItem</a>



<a href="_win32_Tree_View_Controls">Tree-View Controls</a>
 

 

