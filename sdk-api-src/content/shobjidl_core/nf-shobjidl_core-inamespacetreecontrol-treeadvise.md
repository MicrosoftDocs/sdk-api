---
UID: NF:shobjidl_core.INameSpaceTreeControl.TreeAdvise
title: INameSpaceTreeControl::TreeAdvise (shobjidl_core.h)
description: Enables a client to register with the control.
helpviewer_keywords: ["INameSpaceTreeControl interface [Windows Shell]","TreeAdvise method","INameSpaceTreeControl.TreeAdvise","INameSpaceTreeControl::TreeAdvise","TreeAdvise","TreeAdvise method [Windows Shell]","TreeAdvise method [Windows Shell]","INameSpaceTreeControl interface","_shell_INameSpaceTreeControl_TreeAdvise","shell.INameSpaceTreeControl_TreeAdvise","shobjidl_core/INameSpaceTreeControl::TreeAdvise"]
old-location: shell\INameSpaceTreeControl_TreeAdvise.htm
tech.root: shell
ms.assetid: d59b9772-7061-4ea5-964a-75deb293b407
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControl interface [Windows Shell],TreeAdvise method, INameSpaceTreeControl.TreeAdvise, INameSpaceTreeControl::TreeAdvise, TreeAdvise, TreeAdvise method [Windows Shell], TreeAdvise method [Windows Shell],INameSpaceTreeControl interface, _shell_INameSpaceTreeControl_TreeAdvise, shell.INameSpaceTreeControl_TreeAdvise, shobjidl_core/INameSpaceTreeControl::TreeAdvise
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
 - INameSpaceTreeControl::TreeAdvise
 - shobjidl_core/INameSpaceTreeControl::TreeAdvise
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
 - INameSpaceTreeControl.TreeAdvise
---

# INameSpaceTreeControl::TreeAdvise


## -description

Enables a client to register with the control.

## -parameters

### -param punk [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the client IUnknown that registers with the control.

### -param pdwCookie [out]

Type: <b>DWORD*</b>

A pointer to the cookie that is passed back for registration.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The pointer to the cookie that is passed back is used to unregister the control later with <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inamespacetreecontrol-treeunadvise">INameSpaceTreeControl::TreeUnadvise</a>.