---
UID: NF:shobjidl_core.IFolderView.Item
title: IFolderView::Item
author: windows-sdk-content
description: Gets the identifier of a specific item in the folder view, by index.
old-location: shell\IFolderView_Item.htm
old-project: shell
ms.assetid: c130ef36-1255-4c57-be31-7fc2029d9f66
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IFolderView interface [Windows Shell],Item method, IFolderView.Item, IFolderView::Item, Item, Item method [Windows Shell], Item method [Windows Shell],IFolderView interface, _shell_IFolderView_Item, shell.IFolderView_Item, shobjidl_core/IFolderView::Item
ms.prod: windows
ms.technology: windows-sdk
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
 - IFolderView.Item
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# IFolderView::Item


## -description


Gets the identifier of a specific item in the folder view, by index.


## -parameters




### -param iItemIndex [in]

Type: <b>int</b>

The index of the item in the view.


### -param ppidl [out]

Type: <b>PITEMID_CHILD*</b>


          The address of a pointer to a PIDL containing the item's identifier information.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




        When no longer needed, the PIDL should be freed by calling <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>





## -see-also




<a href="https://msdn.microsoft.com/3bc2615e-f07c-4959-b89e-bbbd2bf45a94">IFolderView</a>



<a href="https://msdn.microsoft.com/f93e2d30-7b50-48e8-a3e7-6fa29abb8a32">IFolderView::Items</a>
 

 

