---
UID: NF:shlobj_core.IShellFolderView.AddObject
title: IShellFolderView::AddObject
author: windows-sdk-content
description: AddObject may be altered or unavailable.
old-location: shell\IShellFolderView_AddObject.htm
old-project: shell
ms.assetid: 50f07c12-7c66-40a0-b710-a4240fde859a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AddObject, AddObject method [Windows Shell], AddObject method [Windows Shell],IShellFolderView interface, IShellFolderView interface [Windows Shell],AddObject method, IShellFolderView.AddObject, IShellFolderView::AddObject, _shell_IShellFolderView_AddObject, shell.IShellFolderView_AddObject, shlobj_core/IShellFolderView::AddObject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shlobj_core.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AUTOCOMPLETELISTOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shlobj_core.h
api_name:
 - IShellFolderView.AddObject
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellFolderView::AddObject


## -description


<p class="CCE_Message">[<b>AddObject</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Adds an item to the view.


## -parameters




### -param pidl [in]

Type: <b>PUITEMID_CHILD</b>

A pointer to an ItemID that specifies the item to add to the view.


### -param puItem [out]

Type: <b>UINT*</b>

A pointer to a value that, when this method returns successfully, receives the index position of the added item.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If you immediately call <a href="https://msdn.microsoft.com/a231e92f-b467-4fd7-929d-92259272a734">IShellFolderView::GetObject</a> with this index, you will get a copy of the ITEMID_CHILD that you added.  However, the index position of an item may change over time, so code cannot trust that any specific index always returns the same ITEMID_CHILD.

Items added through this method can be removed from the view by the data source at any time.



