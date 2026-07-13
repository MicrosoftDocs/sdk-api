---
UID: NF:shobjidl_core.IFolderView.ItemCount
title: IFolderView::ItemCount (shobjidl_core.h)
description: Gets the number of items in the folder. This can be the number of all items, or a subset such as the number of selected items.
helpviewer_keywords: ["IFolderView interface [Windows Shell]","ItemCount method","IFolderView.ItemCount","IFolderView::ItemCount","ItemCount","ItemCount method [Windows Shell]","ItemCount method [Windows Shell]","IFolderView interface","_shell_IFolderView_ItemCount","shell.IFolderView_ItemCount","shobjidl_core/IFolderView::ItemCount"]
old-location: shell\IFolderView_ItemCount.htm
tech.root: shell
ms.assetid: dadf91c5-7d27-4b1b-875b-6f0615440f47
ms.date: 12/05/2018
ms.keywords: IFolderView interface [Windows Shell],ItemCount method, IFolderView.ItemCount, IFolderView::ItemCount, ItemCount, ItemCount method [Windows Shell], ItemCount method [Windows Shell],IFolderView interface, _shell_IFolderView_ItemCount, shell.IFolderView_ItemCount, shobjidl_core/IFolderView::ItemCount
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFolderView::ItemCount
 - shobjidl_core/IFolderView::ItemCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IFolderView.ItemCount
---

# IFolderView::ItemCount


## -description

Gets the number of items in the folder. This can be the number of all items, or a subset such as the number of selected items.

## -parameters

### -param uFlags [in]

Type: <b>UINT</b>

Flags from the <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_svgio">_SVGIO</a> enumeration that limit the count to certain types of items.

### -param pcItems [out]

Type: <b>int*</b>

Pointer to an integer that receives the number of items (files and folders) displayed in the folder view.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

