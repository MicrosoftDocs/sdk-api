---
UID: NF:shobjidl.IFolderViewHost.Initialize
title: IFolderViewHost::Initialize (shobjidl.h)
description: Initializes the object that hosts an IFolderView object.
helpviewer_keywords: ["IFolderViewHost interface [Windows Shell]","Initialize method","IFolderViewHost.Initialize","IFolderViewHost::Initialize","Initialize","Initialize method [Windows Shell]","Initialize method [Windows Shell]","IFolderViewHost interface","_shell_IFolderViewHost_Initialize","shell.IFolderViewHost_Initialize","shobjidl/IFolderViewHost::Initialize"]
old-location: shell\IFolderViewHost_Initialize.htm
tech.root: shell
ms.assetid: 77740dfc-6423-451d-859b-7c894122309d
ms.date: 12/05/2018
ms.keywords: IFolderViewHost interface [Windows Shell],Initialize method, IFolderViewHost.Initialize, IFolderViewHost::Initialize, Initialize, Initialize method [Windows Shell], Initialize method [Windows Shell],IFolderViewHost interface, _shell_IFolderViewHost_Initialize, shell.IFolderViewHost_Initialize, shobjidl/IFolderViewHost::Initialize
req.header: shobjidl.h
req.include-header: 
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
 - IFolderViewHost::Initialize
 - shobjidl/IFolderViewHost::Initialize
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
 - IFolderViewHost.Initialize
---

# IFolderViewHost::Initialize


## -description

Initializes the object that hosts an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview">IFolderView</a> object.

## -parameters

### -param hwndParent [in]

Type: <b>HWND</b>

The handle of the window that contains the <a href="/windows/desktop/api/shobjidl/nn-shobjidl-ifolderviewhost">IFolderViewHost</a> object.

### -param pdo [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>*</b>

The address of a pointer to a data object.

### -param prc [in]

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

The address of a pointer to a <b>RECT</b> structure that specifies the dimensions of the folder view.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.