---
UID: NF:shobjidl_core.INamespaceWalkCB.EnterFolder
title: INamespaceWalkCB::EnterFolder (shobjidl_core.h)
description: Called when a folder is about to be entered during a namespace walk. Use this method for any initialization of the retrieved item.
helpviewer_keywords: ["EnterFolder","EnterFolder method [Windows Shell]","EnterFolder method [Windows Shell]","INamespaceWalkCB interface","INamespaceWalkCB interface [Windows Shell]","EnterFolder method","INamespaceWalkCB.EnterFolder","INamespaceWalkCB::EnterFolder","_win32_INamespaceWalkCB_EnterFolder","shell.INamespaceWalkCB_EnterFolder","shobjidl_core/INamespaceWalkCB::EnterFolder"]
old-location: shell\INamespaceWalkCB_EnterFolder.htm
tech.root: shell
ms.assetid: fd5c25f4-6e48-494b-9d5b-ba1d846ce4d2
ms.date: 12/05/2018
ms.keywords: EnterFolder, EnterFolder method [Windows Shell], EnterFolder method [Windows Shell],INamespaceWalkCB interface, INamespaceWalkCB interface [Windows Shell],EnterFolder method, INamespaceWalkCB.EnterFolder, INamespaceWalkCB::EnterFolder, _win32_INamespaceWalkCB_EnterFolder, shell.INamespaceWalkCB_EnterFolder, shobjidl_core/INamespaceWalkCB::EnterFolder
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
 - INamespaceWalkCB::EnterFolder
 - shobjidl_core/INamespaceWalkCB::EnterFolder
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
 - INamespaceWalkCB.EnterFolder
---

# INamespaceWalkCB::EnterFolder


## -description

Called when a folder is about to be entered during a namespace walk. Use this method for any initialization of the retrieved item.

## -parameters

### -param psf [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>*</b>

A pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> object representing the parent of the folder designated by <i>pidl</i>.

### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

The PIDL, relative to <i>psf</i>, of the folder being entered.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.