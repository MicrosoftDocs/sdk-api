---
UID: NF:shobjidl_core.IFolderView.GetItemPosition
title: IFolderView::GetItemPosition (shobjidl_core.h)

description: Gets the position of an item in the folder's view.
old-location: shell\IFolderView_GetItemPosition.htm
tech.root: shell
ms.assetid: 454d074c-1044-4626-8ec7-18e2adb4beca

ms.date: 12/05/2018
ms.keywords: GetItemPosition, GetItemPosition method [Windows Shell], GetItemPosition method [Windows Shell],IFolderView interface, IFolderView interface [Windows Shell],GetItemPosition method, IFolderView.GetItemPosition, IFolderView::GetItemPosition, _shell_IFolderView_GetItemPosition, shell.IFolderView_GetItemPosition, shobjidl_core/IFolderView::GetItemPosition
ms.topic: method
f1_keywords:
- shobjidl_core/IFolderView.GetItemPosition
dev_langs:
 - c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shell32.dll
api_name:
- IFolderView.GetItemPosition
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFolderView::GetItemPosition


## -description


Gets the position of an item in the folder's view.


## -parameters




### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> interface.


### -param ppt [out]

Type: <b><a href="https://docs.microsoft.com/previous-versions/dd162805(v=vs.85)">POINT</a>*</b>

A pointer to a structure that receives the position of the item's upper-left corner.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



