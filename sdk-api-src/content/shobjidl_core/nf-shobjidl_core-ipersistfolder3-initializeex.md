---
UID: NF:shobjidl_core.IPersistFolder3.InitializeEx
title: IPersistFolder3::InitializeEx (shobjidl_core.h)
description: Initializes a folder and specifies its location in the namespace. If the folder is a shortcut, this method also specifies the location of the target folder.
helpviewer_keywords: ["IPersistFolder3 interface [Windows Shell]","InitializeEx method","IPersistFolder3.InitializeEx","IPersistFolder3::InitializeEx","InitializeEx","InitializeEx method [Windows Shell]","InitializeEx method [Windows Shell]","IPersistFolder3 interface","_win32_IPersistFolder3_InitializeEx","shell.IPersistFolder3_InitializeEx","shobjidl_core/IPersistFolder3::InitializeEx"]
old-location: shell\IPersistFolder3_InitializeEx.htm
tech.root: shell
ms.assetid: 50a426b5-a526-4d3d-a20a-67050229f02e
ms.date: 12/05/2018
ms.keywords: IPersistFolder3 interface [Windows Shell],InitializeEx method, IPersistFolder3.InitializeEx, IPersistFolder3::InitializeEx, InitializeEx, InitializeEx method [Windows Shell], InitializeEx method [Windows Shell],IPersistFolder3 interface, _win32_IPersistFolder3_InitializeEx, shell.IPersistFolder3_InitializeEx, shobjidl_core/IPersistFolder3::InitializeEx
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional with SP3, Windows XP [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPersistFolder3::InitializeEx
 - shobjidl_core/IPersistFolder3::InitializeEx
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
 - IPersistFolder3.InitializeEx
---

# IPersistFolder3::InitializeEx


## -description

Initializes a folder and specifies its location in the namespace. If the folder is a shortcut, this method also specifies the location of the target folder.

## -parameters

### -param pbc [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>*</b>

A pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a> object that provides the bind context. This parameter can be <b>NULL</b>.

### -param pidlRoot [in]

Type: <b>LPCITEMIDLIST</b>

A pointer to a fully qualified PIDL that specifies the absolute location of a folder or folder shortcut. The calling application is responsible for allocating and freeing this PIDL.

### -param ppfti [in]

Type: <b>const <a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-persist_folder_target_info">PERSIST_FOLDER_TARGET_INFO</a>*</b>

A pointer to a <a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-persist_folder_target_info">PERSIST_FOLDER_TARGET_INFO</a> structure that specifies the location of the target folder and its attributes. 

                    

If <i>ppfti</i> points to a valid structure, <i>pidlRoot</i> represents a folder shortcut.

If <i>ppfti</i> is set to <b>NULL</b>, <i>pidlRoot</i> represents a normal folder. In that case, <b>InitializeEx</b> should behave as if <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize">Initialize</a> had been called.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function is an extended version of <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize">IPersistFolder::Initialize</a>. It allows the Shell to initialize folder shortcuts as well as normal folders.