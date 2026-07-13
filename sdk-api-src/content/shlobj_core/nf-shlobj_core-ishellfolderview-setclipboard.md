---
UID: NF:shlobj_core.IShellFolderView.SetClipboard
title: IShellFolderView::SetClipboard (shlobj_core.h)
description: SetClipboard may be altered or unavailable.
helpviewer_keywords: ["IShellFolderView interface [Windows Shell]","SetClipboard method","IShellFolderView.SetClipboard","IShellFolderView::SetClipboard","SetClipboard","SetClipboard method [Windows Shell]","SetClipboard method [Windows Shell]","IShellFolderView interface","_shell_IShellFolderView_SetClipboard","shell.IShellFolderView_SetClipboard","shlobj_core/IShellFolderView::SetClipboard"]
old-location: shell\IShellFolderView_SetClipboard.htm
tech.root: shell
ms.assetid: 372cc6db-f9c1-4110-98aa-a7ad90312048
ms.date: 12/05/2018
ms.keywords: IShellFolderView interface [Windows Shell],SetClipboard method, IShellFolderView.SetClipboard, IShellFolderView::SetClipboard, SetClipboard, SetClipboard method [Windows Shell], SetClipboard method [Windows Shell],IShellFolderView interface, _shell_IShellFolderView_SetClipboard, shell.IShellFolderView_SetClipboard, shlobj_core/IShellFolderView::SetClipboard
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
 - IShellFolderView::SetClipboard
 - shlobj_core/IShellFolderView::SetClipboard
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shlobj_core.h
api_name:
 - IShellFolderView.SetClipboard
---

# IShellFolderView::SetClipboard


## -description

<p class="CCE_Message">[<b>SetClipboard</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Performs a cut operation on the current selection.

## -parameters

### -param bMove

Type: <b>BOOL</b>

Must be <b>TRUE</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

