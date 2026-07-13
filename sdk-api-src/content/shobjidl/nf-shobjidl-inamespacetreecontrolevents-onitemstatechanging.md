---
UID: NF:shobjidl.INameSpaceTreeControlEvents.OnItemStateChanging
title: INameSpaceTreeControlEvents::OnItemStateChanging (shobjidl.h)
description: Called before the state of an item changes.
helpviewer_keywords: ["INameSpaceTreeControlEvents interface [Windows Shell]","OnItemStateChanging method","INameSpaceTreeControlEvents.OnItemStateChanging","INameSpaceTreeControlEvents::OnItemStateChanging","OnItemStateChanging","OnItemStateChanging method [Windows Shell]","OnItemStateChanging method [Windows Shell]","INameSpaceTreeControlEvents interface","_shell_INameSpaceTreeControlEvents_OnItemStateChanging","shell.INameSpaceTreeControlEvents_OnItemStateChanging","shobjidl/INameSpaceTreeControlEvents::OnItemStateChanging"]
old-location: shell\INameSpaceTreeControlEvents_OnItemStateChanging.htm
tech.root: shell
ms.assetid: ed0f431a-f3e2-4a95-a16e-6e38568dd91f
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControlEvents interface [Windows Shell],OnItemStateChanging method, INameSpaceTreeControlEvents.OnItemStateChanging, INameSpaceTreeControlEvents::OnItemStateChanging, OnItemStateChanging, OnItemStateChanging method [Windows Shell], OnItemStateChanging method [Windows Shell],INameSpaceTreeControlEvents interface, _shell_INameSpaceTreeControlEvents_OnItemStateChanging, shell.INameSpaceTreeControlEvents_OnItemStateChanging, shobjidl/INameSpaceTreeControlEvents::OnItemStateChanging
req.header: shobjidl.h
req.include-header: 
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
 - INameSpaceTreeControlEvents::OnItemStateChanging
 - shobjidl/INameSpaceTreeControlEvents::OnItemStateChanging
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - INameSpaceTreeControlEvents.OnItemStateChanging
---

# INameSpaceTreeControlEvents::OnItemStateChanging


## -description

Called before the state of an item changes.

## -parameters

### -param psi [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the Shell item for which the state is going to change.

### -param nstcisMask [in]

Type: <b><a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_nstcitemstate">NSTCITEMSTATE</a></b>

One or more values from the <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_nstcitemstate">NSTCITEMSTATE</a> enumeration that indicate which pieces of information the calling application wants to set.

### -param nstcisState [in]

Type: <b><a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_nstcitemstate">NSTCITEMSTATE</a></b>

One or more values from the <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_nstcitemstate">NSTCITEMSTATE</a> enumeration that indicate the values that are to be set.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.