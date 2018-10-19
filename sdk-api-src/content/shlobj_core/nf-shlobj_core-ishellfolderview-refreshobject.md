---
UID: NF:shlobj_core.IShellFolderView.RefreshObject
title: IShellFolderView::RefreshObject
author: windows-sdk-content
description: RefreshObject may be altered or unavailable.
old-location: shell\IShellFolderView_RefreshObject.htm
tech.root: shell
ms.assetid: 6165d2d1-4bd6-4a18-8191-1fd7e924d7d8
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: IShellFolderView interface [Windows Shell],RefreshObject method, IShellFolderView.RefreshObject, IShellFolderView::RefreshObject, RefreshObject, RefreshObject method [Windows Shell], RefreshObject method [Windows Shell],IShellFolderView interface, _shell_IShellFolderView_RefreshObject, shell.IShellFolderView_RefreshObject, shlobj_core/IShellFolderView::RefreshObject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shlobj_core.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shlobj_core.h
api_name:
 - IShellFolderView.RefreshObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellFolderView::RefreshObject


## -description


<p class="CCE_Message">[<b>RefreshObject</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Redraws the given item.


## -parameters




### -param pidl [in]

Type: <b>PUITEMID_CHILD</b>

The item to be redrawn.


### -param puItem [out]

Type: <b>UINT*</b>

A pointer to a value that, when this method returns successfully, receives the index of the item that was redrawn. You can use this value to call <a href="https://msdn.microsoft.com/a231e92f-b467-4fd7-929d-92259272a734">IShellFolderView::GetObject</a> to retrieve the PITEMID_CHILD that you just redrew.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If you immediately call <a href="https://msdn.microsoft.com/a231e92f-b467-4fd7-929d-92259272a734">IShellFolderView::GetObject</a> with the index returned by <i>puItem</i>, you will get a copy of the ITEMID_CHILD that you redrew.  However, the index position of an item may change over time, so code cannot trust that any specific index always returns the same ITEMID_CHILD.



