---
UID: NF:shobjidl_core.INameSpaceTreeControl.GetItemRect
title: INameSpaceTreeControl::GetItemRect (shobjidl_core.h)
description: Gets the RECT structure that describes the size and position of a given item.
helpviewer_keywords: ["GetItemRect","GetItemRect method [Windows Shell]","GetItemRect method [Windows Shell]","INameSpaceTreeControl interface","INameSpaceTreeControl interface [Windows Shell]","GetItemRect method","INameSpaceTreeControl.GetItemRect","INameSpaceTreeControl::GetItemRect","_shell_INameSpaceTreeControl_GetItemRect","shell.INameSpaceTreeControl_GetItemRect","shobjidl_core/INameSpaceTreeControl::GetItemRect"]
old-location: shell\INameSpaceTreeControl_GetItemRect.htm
tech.root: shell
ms.assetid: 57e7707c-0fe2-4cde-87d8-2d58e7c06bba
ms.date: 12/05/2018
ms.keywords: GetItemRect, GetItemRect method [Windows Shell], GetItemRect method [Windows Shell],INameSpaceTreeControl interface, INameSpaceTreeControl interface [Windows Shell],GetItemRect method, INameSpaceTreeControl.GetItemRect, INameSpaceTreeControl::GetItemRect, _shell_INameSpaceTreeControl_GetItemRect, shell.INameSpaceTreeControl_GetItemRect, shobjidl_core/INameSpaceTreeControl::GetItemRect
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
 - INameSpaceTreeControl::GetItemRect
 - shobjidl_core/INameSpaceTreeControl::GetItemRect
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
 - INameSpaceTreeControl.GetItemRect
---

# INameSpaceTreeControl::GetItemRect


## -description

Gets the <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that describes the size and position of a given item.

## -parameters

### -param psi [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the item for which the <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure is being retrieved.

### -param prect [out]

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

A pointer to the <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that describes the size and position of the item.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.