---
UID: NF:shobjidl_core.IFolderView.SelectAndPositionItems
title: IFolderView::SelectAndPositionItems (shobjidl_core.h)
description: Allows the selection and positioning of items visible in the folder's view.
old-location: shell\IFolderView_SelectAndPositionItems.htm
tech.root: shell
ms.assetid: 1263bba8-63c8-4630-ab59-bb4ae10061fc
ms.date: 12/05/2018
ms.keywords: IFolderView interface [Windows Shell],SelectAndPositionItems method, IFolderView.SelectAndPositionItems, IFolderView::SelectAndPositionItems, SelectAndPositionItems, SelectAndPositionItems method [Windows Shell], SelectAndPositionItems method [Windows Shell],IFolderView interface, _shell_IFolderView_SelectAndPositionItems, shell.IFolderView_SelectAndPositionItems, shobjidl_core/IFolderView::SelectAndPositionItems
ms.topic: method
f1_keywords:
- shobjidl_core/IFolderView.SelectAndPositionItems
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
- IFolderView.SelectAndPositionItems
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFolderView::SelectAndPositionItems


## -description


Allows the selection and positioning of items visible in the folder's view.


## -parameters




### -param cidl [in]

Type: <b>UINT</b>

The number of items to select.


### -param apidl [in]

Type: <b>PCUITEMID_CHILD_ARRAY*</b>

A pointer to an array of size <i>cidl</i> that contains the PIDLs of the items.


### -param apt [in]

Type: <b><a href="https://docs.microsoft.com/previous-versions/dd162805(v=vs.85)">POINT</a>*</b>

A pointer to an array of <i>cidl</i> structures containing the locations each corresponding element in <i>apidl</i> should be positioned.


### -param dwFlags [in]

Type: <b>DWORD</b>

One of the <a href="https://docs.microsoft.com/windows/win32/api/shobjidl_core/ne-shobjidl_core-_svsif">_SVSIF</a> constants that specifies the type of selection to apply.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/ne-shobjidl-folderviewoptions">FOLDERVIEWOPTIONS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview">IFolderView</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-selectitem">IFolderView::SelectItem</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-selectitem">SelectItem</a>
 

 

