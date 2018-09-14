---
UID: NF:shobjidl_core.IFolderView.GetFocusedItem
title: IFolderView::GetFocusedItem
author: windows-sdk-content
description: Gets the index of the item that currently has focus in the folder's view.
old-location: shell\IFolderView_GetFocusedItem.htm
tech.root: shell
ms.assetid: 5bbc0baf-b384-41da-850c-b2cb9570cb69
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: GetFocusedItem, GetFocusedItem method [Windows Shell], GetFocusedItem method [Windows Shell],IFolderView interface, IFolderView interface [Windows Shell],GetFocusedItem method, IFolderView.GetFocusedItem, IFolderView::GetFocusedItem, _shell_IFolderView_GetFocusedItem, shell.IFolderView_GetFocusedItem, shobjidl_core/IFolderView::GetFocusedItem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IFolderView.GetFocusedItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFolderView::GetFocusedItem


## -description


Gets the index of the item that currently has focus in the folder's view.


## -parameters




### -param piItem [out]

Type: <b>int*</b>

A pointer to the index of the item.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



