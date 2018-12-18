---
UID: NF:shobjidl_core.IFolderView.SelectItem
title: IFolderView::SelectItem
author: windows-sdk-content
description: Selects an item in the folder's view.
old-location: shell\IFolderView_SelectItem.htm
tech.root: shell
ms.assetid: 6db262ea-861b-4bc5-955f-b81945313ea8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFolderView interface [Windows Shell],SelectItem method, IFolderView.SelectItem, IFolderView::SelectItem, SelectItem, SelectItem method [Windows Shell], SelectItem method [Windows Shell],IFolderView interface, _shell_IFolderView_SelectItem, shell.IFolderView_SelectItem, shobjidl_core/IFolderView::SelectItem
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
 - IFolderView.SelectItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFolderView::SelectItem


## -description


Selects an item in the folder's view.


## -parameters




### -param iItem [in]

Type: <b>int</b>

The index of the item to select in the folder's view.


### -param dwFlags [in]

Type: <b>DWORD</b>

One of the <a href="https://msdn.microsoft.com/3b0a7ec3-f365-48ec-86b0-ffd4c345deaf">_SVSIF</a> constants that specify the type of selection to apply.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3bc2615e-f07c-4959-b89e-bbbd2bf45a94">IFolderView</a>



<a href="https://msdn.microsoft.com/86416704-c2e3-4782-a566-b49cbd0e7696">IFolderView::GetSelectionMarkedItem</a>



<a href="https://msdn.microsoft.com/1263bba8-63c8-4630-ab59-bb4ae10061fc">IFolderView::SelectAndPositionItems</a>



<a href="https://msdn.microsoft.com/5c34c05e-175c-43cb-9fbb-2eb3e2b39f6f">SelectItem</a>
 

 

