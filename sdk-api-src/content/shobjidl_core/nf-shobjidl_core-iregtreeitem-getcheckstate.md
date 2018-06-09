---
UID: NF:shobjidl_core.IRegTreeItem.GetCheckState
title: IRegTreeItem::GetCheckState
author: windows-sdk-content
description: Gets the state of a check box item in a tree-view control.
old-location: shell\IRegTreeItem_GetCheckState.htm
old-project: shell
ms.assetid: bfeff83e-8872-4df2-a519-1335be6e443c
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: FALSE, GetCheckState, GetCheckState method [Windows Shell], GetCheckState method [Windows Shell],IRegTreeItem interface, IRegTreeItem interface [Windows Shell],GetCheckState method, IRegTreeItem.GetCheckState, IRegTreeItem::GetCheckState, TRUE, _win32_IRegTreeItem_GetCheckState, shell.IRegTreeItem_GetCheckState, shobjidl_core/IRegTreeItem::GetCheckState
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IRegTreeItem.GetCheckState
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IRegTreeItem::GetCheckState


## -description


Gets the state of a check box item in a tree-view control.


## -parameters




### -param pbCheck [out]

Type: <b>BOOL*</b>

A pointer to a <b>BOOL</b> that contains the state of the check box.



#### TRUE

The check box is checked.



#### FALSE

The check box is not checked.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/a9ae0fb3-4a6e-473e-9fa3-d3894834fb72">IRegTreeItem</a>



<a href="https://www.bing.com/search?q=Tree-View+Controls">Tree-View Controls</a>
 

 

