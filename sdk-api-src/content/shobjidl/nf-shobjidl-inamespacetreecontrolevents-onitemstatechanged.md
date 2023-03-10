---
UID: NF:shobjidl.INameSpaceTreeControlEvents.OnItemStateChanged
title: INameSpaceTreeControlEvents::OnItemStateChanged (shobjidl.h)
description: Not implemented. (INameSpaceTreeControlEvents.OnItemStateChanged)
helpviewer_keywords: ["INameSpaceTreeControlEvents interface [Windows Shell]","OnItemStateChanged method","INameSpaceTreeControlEvents.OnItemStateChanged","INameSpaceTreeControlEvents::OnItemStateChanged","OnItemStateChanged","OnItemStateChanged method [Windows Shell]","OnItemStateChanged method [Windows Shell]","INameSpaceTreeControlEvents interface","_shell_INameSpaceTreeControlEvents_OnItemStateChanged","shell.INameSpaceTreeControlEvents_OnItemStateChanged","shobjidl/INameSpaceTreeControlEvents::OnItemStateChanged"]
old-location: shell\INameSpaceTreeControlEvents_OnItemStateChanged.htm
tech.root: shell
ms.assetid: 0154d97b-44db-40bf-a202-e97ba318555f
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControlEvents interface [Windows Shell],OnItemStateChanged method, INameSpaceTreeControlEvents.OnItemStateChanged, INameSpaceTreeControlEvents::OnItemStateChanged, OnItemStateChanged, OnItemStateChanged method [Windows Shell], OnItemStateChanged method [Windows Shell],INameSpaceTreeControlEvents interface, _shell_INameSpaceTreeControlEvents_OnItemStateChanged, shell.INameSpaceTreeControlEvents_OnItemStateChanged, shobjidl/INameSpaceTreeControlEvents::OnItemStateChanged
req.header: shobjidl.h
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
 - INameSpaceTreeControlEvents::OnItemStateChanged
 - shobjidl/INameSpaceTreeControlEvents::OnItemStateChanged
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl.h
api_name:
 - INameSpaceTreeControlEvents.OnItemStateChanged
---

# INameSpaceTreeControlEvents::OnItemStateChanged


## -description

Not implemented.

## -parameters

### -param psi [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the shell item for which the state has changed.

### -param nstcisMask [in]

Type: <b><a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_nstcitemstate">NSTCITEMSTATE</a></b>

One or more values from the <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_nstcitemstate">NSTCITEMSTATE</a> enumeration that indicates what pieces of information the caller wants to set.

### -param nstcisState [in]

Type: <b><a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_nstcitemstate">NSTCITEMSTATE</a></b>

One or more values from the <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_nstcitemstate">NSTCITEMSTATE</a> enumeration that indicates the values that are to be set.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
