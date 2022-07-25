---
UID: NF:shobjidl_core.INameSpaceTreeControl.Initialize
title: INameSpaceTreeControl::Initialize (shobjidl_core.h)
description: Initializes an INameSpaceTreeControl object.
helpviewer_keywords: ["INameSpaceTreeControl interface [Windows Shell]","Initialize method","INameSpaceTreeControl.Initialize","INameSpaceTreeControl::Initialize","Initialize","Initialize method [Windows Shell]","Initialize method [Windows Shell]","INameSpaceTreeControl interface","_shell_INameSpaceTreeControl_Initialize","shell.INameSpaceTreeControl_Initialize","shobjidl_core/INameSpaceTreeControl::Initialize"]
old-location: shell\INameSpaceTreeControl_Initialize.htm
tech.root: shell
ms.assetid: dfc602bd-6e4e-492d-8bf4-1499319adee7
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControl interface [Windows Shell],Initialize method, INameSpaceTreeControl.Initialize, INameSpaceTreeControl::Initialize, Initialize, Initialize method [Windows Shell], Initialize method [Windows Shell],INameSpaceTreeControl interface, _shell_INameSpaceTreeControl_Initialize, shell.INameSpaceTreeControl_Initialize, shobjidl_core/INameSpaceTreeControl::Initialize
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
 - INameSpaceTreeControl::Initialize
 - shobjidl_core/INameSpaceTreeControl::Initialize
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
 - INameSpaceTreeControl.Initialize
---

# INameSpaceTreeControl::Initialize


## -description

Initializes an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol">INameSpaceTreeControl</a> object.

## -parameters

### -param hwndParent [in]

Type: <b>HWND</b>

The handle of the parent window.

### -param prc [in]

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that describes the size and position of the control in the client window.

### -param nsctsFlags [in]

Type: <b><a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_nstcstyle">NSTCSTYLE</a></b>

The characteristics of the given namespace tree control. One or more of the following values from the <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_nstcstyle">NSTCSTYLE</a> enumeration.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.