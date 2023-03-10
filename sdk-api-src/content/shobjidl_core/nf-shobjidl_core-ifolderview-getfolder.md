---
UID: NF:shobjidl_core.IFolderView.GetFolder
title: IFolderView::GetFolder (shobjidl_core.h)
description: Gets the folder object.
helpviewer_keywords: ["GetFolder","GetFolder method [Windows Shell]","GetFolder method [Windows Shell]","IFolderView interface","IFolderView interface [Windows Shell]","GetFolder method","IFolderView.GetFolder","IFolderView::GetFolder","_shell_IFolderView_GetFolder","shell.IFolderView_GetFolder","shobjidl_core/IFolderView::GetFolder"]
old-location: shell\IFolderView_GetFolder.htm
tech.root: shell
ms.assetid: 4fdeb995-2220-4461-a4d6-80bce08153b1
ms.date: 12/05/2018
ms.keywords: GetFolder, GetFolder method [Windows Shell], GetFolder method [Windows Shell],IFolderView interface, IFolderView interface [Windows Shell],GetFolder method, IFolderView.GetFolder, IFolderView::GetFolder, _shell_IFolderView_GetFolder, shell.IFolderView_GetFolder, shobjidl_core/IFolderView::GetFolder
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
 - IFolderView::GetFolder
 - shobjidl_core/IFolderView::GetFolder
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
 - IFolderView.GetFolder
---

# IFolderView::GetFolder


## -description

Gets the folder object.

## -parameters

### -param riid [in]

Type: <b>REFIID</b>

Reference to the desired IID to represent the folder.

### -param ppv [out]

Type: <b>VOID**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>. This is typically <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> or a related interface. This can also be an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a> with a single element.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.