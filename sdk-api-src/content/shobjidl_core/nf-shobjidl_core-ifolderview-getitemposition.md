---
UID: NF:shobjidl_core.IFolderView.GetItemPosition
title: IFolderView::GetItemPosition (shobjidl_core.h)
description: Gets the position of an item in the folder's view.
helpviewer_keywords: ["GetItemPosition","GetItemPosition method [Windows Shell]","GetItemPosition method [Windows Shell]","IFolderView interface","IFolderView interface [Windows Shell]","GetItemPosition method","IFolderView.GetItemPosition","IFolderView::GetItemPosition","_shell_IFolderView_GetItemPosition","shell.IFolderView_GetItemPosition","shobjidl_core/IFolderView::GetItemPosition"]
old-location: shell\IFolderView_GetItemPosition.htm
tech.root: shell
ms.assetid: 454d074c-1044-4626-8ec7-18e2adb4beca
ms.date: 12/05/2018
ms.keywords: GetItemPosition, GetItemPosition method [Windows Shell], GetItemPosition method [Windows Shell],IFolderView interface, IFolderView interface [Windows Shell],GetItemPosition method, IFolderView.GetItemPosition, IFolderView::GetItemPosition, _shell_IFolderView_GetItemPosition, shell.IFolderView_GetItemPosition, shobjidl_core/IFolderView::GetItemPosition
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IFolderView::GetItemPosition
 - shobjidl_core/IFolderView::GetItemPosition
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
 - IFolderView.GetItemPosition
---

# IFolderView::GetItemPosition


## -description

Gets the position of an item in the folder's view.

## -parameters

### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

A pointer to an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> interface.

### -param ppt [out]

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a>*</b>

A pointer to a structure that receives the position of the item's upper-left corner.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.