---
UID: NF:shlobj_core.IShellFolderView.SetRedraw
title: IShellFolderView::SetRedraw (shlobj_core.h)
description: Allows a view to be redrawn or prevents it from being redrawn.
helpviewer_keywords: ["IShellFolderView interface [Windows Shell]","SetRedraw method","IShellFolderView.SetRedraw","IShellFolderView::SetRedraw","SetRedraw","SetRedraw method [Windows Shell]","SetRedraw method [Windows Shell]","IShellFolderView interface","_shell_IShellFolderView_SetRedraw","shell.IShellFolderView_SetRedraw","shlobj_core/IShellFolderView::SetRedraw"]
old-location: shell\IShellFolderView_SetRedraw.htm
tech.root: shell
ms.assetid: fe249faa-561f-4179-a478-4ff284ffa963
ms.date: 12/05/2018
ms.keywords: IShellFolderView interface [Windows Shell],SetRedraw method, IShellFolderView.SetRedraw, IShellFolderView::SetRedraw, SetRedraw, SetRedraw method [Windows Shell], SetRedraw method [Windows Shell],IShellFolderView interface, _shell_IShellFolderView_SetRedraw, shell.IShellFolderView_SetRedraw, shlobj_core/IShellFolderView::SetRedraw
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
 - IShellFolderView::SetRedraw
 - shlobj_core/IShellFolderView::SetRedraw
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
 - IShellFolderView.SetRedraw
---

# IShellFolderView::SetRedraw


## -description

<p class="CCE_Message">[This method is available through Windows Vista. It might be altered or unavailable in subsequent versions of Windows.]

Allows a view to be redrawn or prevents it from being redrawn.

## -parameters

### -param bRedraw

Type: <b>BOOL</b>

<b>TRUE</b> if the content can be redrawn after a change; <b>FALSE</b> if the content cannot be redrawn after a change.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method sends the <a href="/windows/desktop/gdi/wm-setredraw">WM_SETREDRAW</a> message to the ListView object that the view contains.