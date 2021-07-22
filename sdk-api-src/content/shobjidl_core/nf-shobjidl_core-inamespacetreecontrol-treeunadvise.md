---
UID: NF:shobjidl_core.INameSpaceTreeControl.TreeUnadvise
title: INameSpaceTreeControl::TreeUnadvise (shobjidl_core.h)
description: Enables a client to unregister with the control.
helpviewer_keywords: ["INameSpaceTreeControl interface [Windows Shell]","TreeUnadvise method","INameSpaceTreeControl.TreeUnadvise","INameSpaceTreeControl::TreeUnadvise","TreeUnadvise","TreeUnadvise method [Windows Shell]","TreeUnadvise method [Windows Shell]","INameSpaceTreeControl interface","_shell_INameSpaceTreeControl_TreeUnadvise","shell.INameSpaceTreeControl_TreeUnadvise","shobjidl_core/INameSpaceTreeControl::TreeUnadvise"]
old-location: shell\INameSpaceTreeControl_TreeUnadvise.htm
tech.root: shell
ms.assetid: 9a0ba832-503a-48d6-80a7-7f6c51d60215
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControl interface [Windows Shell],TreeUnadvise method, INameSpaceTreeControl.TreeUnadvise, INameSpaceTreeControl::TreeUnadvise, TreeUnadvise, TreeUnadvise method [Windows Shell], TreeUnadvise method [Windows Shell],INameSpaceTreeControl interface, _shell_INameSpaceTreeControl_TreeUnadvise, shell.INameSpaceTreeControl_TreeUnadvise, shobjidl_core/INameSpaceTreeControl::TreeUnadvise
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
 - INameSpaceTreeControl::TreeUnadvise
 - shobjidl_core/INameSpaceTreeControl::TreeUnadvise
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
 - INameSpaceTreeControl.TreeUnadvise
---

# INameSpaceTreeControl::TreeUnadvise


## -description

Enables a client to unregister with the control.

## -parameters

### -param dwCookie [in]

Type: <b>DWORD*</b>

A pointer to the cookie that is to be unregistered.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The pointer to the cookie that is passed in is the one that was passed back in <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inamespacetreecontrol-treeadvise">INameSpaceTreeControl::TreeAdvise</a>.