---
UID: NF:shobjidl_core.ISearchFolderItemFactory.GetShellItem
title: ISearchFolderItemFactory::GetShellItem (shobjidl_core.h)
description: Gets the search folder as a IShellItem.
helpviewer_keywords: ["GetShellItem","GetShellItem method [Windows Shell]","GetShellItem method [Windows Shell]","ISearchFolderItemFactory interface","ISearchFolderItemFactory interface [Windows Shell]","GetShellItem method","ISearchFolderItemFactory.GetShellItem","ISearchFolderItemFactory::GetShellItem","_shell_ISearchFolderItemFactory_GetShellItem","shell.ISearchFolderItemFactory_GetShellItem","shobjidl_core/ISearchFolderItemFactory::GetShellItem"]
old-location: shell\ISearchFolderItemFactory_GetShellItem.htm
tech.root: shell
ms.assetid: fc5dd159-8a47-479f-b087-bd161093d0a0
ms.date: 12/05/2018
ms.keywords: GetShellItem, GetShellItem method [Windows Shell], GetShellItem method [Windows Shell],ISearchFolderItemFactory interface, ISearchFolderItemFactory interface [Windows Shell],GetShellItem method, ISearchFolderItemFactory.GetShellItem, ISearchFolderItemFactory::GetShellItem, _shell_ISearchFolderItemFactory_GetShellItem, shell.ISearchFolderItemFactory_GetShellItem, shobjidl_core/ISearchFolderItemFactory::GetShellItem
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISearchFolderItemFactory::GetShellItem
 - shobjidl_core/ISearchFolderItemFactory::GetShellItem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - ISearchFolderItemFactory.GetShellItem
---

# ISearchFolderItemFactory::GetShellItem


## -description

Gets the search folder as a <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>.

## -parameters

### -param riid [in]

Type: <b>REFIID</b>

A reference to the desired IID.

### -param ppv [out]

Type: <b>void**</b>

The <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> interface pointer specified in <i>riid</i>.

## -returns

Type: <b>HRESULT</b>

Returns a success value if successful, or an error value otherwise.

## -remarks

When the retrieved <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> is enumerated, it returns the search results.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory">ISearchFolderItemFactory</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromidlist">SHCreateItemFromIDList</a>