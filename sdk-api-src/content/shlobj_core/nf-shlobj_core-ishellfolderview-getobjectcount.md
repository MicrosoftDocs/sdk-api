---
UID: NF:shlobj_core.IShellFolderView.GetObjectCount
title: IShellFolderView::GetObjectCount (shlobj_core.h)
description: Gets the number of items in the folder view.
helpviewer_keywords: ["GetObjectCount","GetObjectCount method [Windows Shell]","GetObjectCount method [Windows Shell]","IShellFolderView interface","IShellFolderView interface [Windows Shell]","GetObjectCount method","IShellFolderView.GetObjectCount","IShellFolderView::GetObjectCount","_shell_IShellFolderView_GetObjectCount","shell.IShellFolderView_GetObjectCount","shlobj_core/IShellFolderView::GetObjectCount"]
old-location: shell\IShellFolderView_GetObjectCount.htm
tech.root: shell
ms.assetid: a68dca56-ae89-4280-b1de-8c85362bf9c6
ms.date: 12/05/2018
ms.keywords: GetObjectCount, GetObjectCount method [Windows Shell], GetObjectCount method [Windows Shell],IShellFolderView interface, IShellFolderView interface [Windows Shell],GetObjectCount method, IShellFolderView.GetObjectCount, IShellFolderView::GetObjectCount, _shell_IShellFolderView_GetObjectCount, shell.IShellFolderView_GetObjectCount, shlobj_core/IShellFolderView::GetObjectCount
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IShellFolderView::GetObjectCount
 - shlobj_core/IShellFolderView::GetObjectCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shlobj_core.h
api_name:
 - IShellFolderView.GetObjectCount
---

# IShellFolderView::GetObjectCount


## -description

<p class="CCE_Message">[<b>GetObjectCount</b> is no longer available for use as of Windows Vista. Instead, use <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-itemcount">ItemCount</a>.]

Gets the number of items in the folder view.

## -parameters

### -param puCount [out]

Type: <b>UINT*</b>

When this method returns, contains a pointer to the number of items displayed in the folder view.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.