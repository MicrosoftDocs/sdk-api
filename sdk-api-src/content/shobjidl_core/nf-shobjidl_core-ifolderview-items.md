---
UID: NF:shobjidl_core.IFolderView.Items
title: IFolderView::Items (shobjidl_core.h)
author: windows-sdk-content
description: Gets the address of an enumeration object based on the collection of items in the folder view.
old-location: shell\IFolderView_Items.htm
tech.root: shell
ms.assetid: f93e2d30-7b50-48e8-a3e7-6fa29abb8a32
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFolderView interface [Windows Shell],Items method, IFolderView.Items, IFolderView::Items, Items, Items method [Windows Shell], Items method [Windows Shell],IFolderView interface, _shell_IFolderView_Items, shell.IFolderView_Items, shobjidl_core/IFolderView::Items
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
 - IFolderView.Items
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFolderView::Items


## -description


Gets the address of an enumeration object based on the collection of items in the folder view.


## -parameters




### -param uFlags [in]

Type: <b>UINT</b>


<a href="https://msdn.microsoft.com/06ed616b-8121-4ea0-bd05-632888d0f376">_SVGIO</a> values that limit the enumeration to certain types of items.


### -param riid [in]

Type: <b>REFIID</b>

Reference to the desired IID to represent the folder.


### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>. This is typically an <a href="https://msdn.microsoft.com/b6f139d3-c54c-4350-9d8b-cd534909a488">IEnumIDList</a>, <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>, or <a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a>. If an error occurs, this value is <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3bc2615e-f07c-4959-b89e-bbbd2bf45a94">IFolderView</a>



<a href="https://msdn.microsoft.com/c130ef36-1255-4c57-be31-7fc2029d9f66">IFolderView::Item</a>
 

 

