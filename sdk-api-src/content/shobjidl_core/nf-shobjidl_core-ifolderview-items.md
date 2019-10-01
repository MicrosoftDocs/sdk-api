---
UID: NF:shobjidl_core.IFolderView.Items
title: IFolderView::Items (shobjidl_core.h)
author: windows-sdk-content
description: Gets the address of an enumeration object based on the collection of items in the folder view.
old-location: shell\IFolderView_Items.htm
tech.root: shell
ms.assetid: f93e2d30-7b50-48e8-a3e7-6fa29abb8a32
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFolderView interface [Windows Shell],Items method, IFolderView.Items, IFolderView::Items, Items, Items method [Windows Shell], Items method [Windows Shell],IFolderView interface, _shell_IFolderView_Items, shell.IFolderView_Items, shobjidl_core/IFolderView::Items
ms.topic: method
f1_keywords: 
 - "shobjidl_core/IFolderView.Items"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFolderView::Items


## -description


Gets the address of an enumeration object based on the collection of items in the folder view.


## -parameters




### -param uFlags [in]

Type: <b>UINT</b>


<a href="https://docs.microsoft.com/windows/win32/api/shobjidl_core/ne-shobjidl_core-_svgio">_SVGIO</a> values that limit the enumeration to certain types of items.


### -param riid [in]

Type: <b>REFIID</b>

Reference to the desired IID to represent the folder.


### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>. This is typically an <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist">IEnumIDList</a>, <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>. If an error occurs, this value is <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview">IFolderView</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-item">IFolderView::Item</a>
 

 

