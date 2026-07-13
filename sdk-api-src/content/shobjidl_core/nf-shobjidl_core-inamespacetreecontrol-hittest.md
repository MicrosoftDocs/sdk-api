---
UID: NF:shobjidl_core.INameSpaceTreeControl.HitTest
title: INameSpaceTreeControl::HitTest (shobjidl_core.h)
description: Retrieves the item that a given point is in, if any.
helpviewer_keywords: ["HitTest","HitTest method [Windows Shell]","HitTest method [Windows Shell]","INameSpaceTreeControl interface","INameSpaceTreeControl interface [Windows Shell]","HitTest method","INameSpaceTreeControl.HitTest","INameSpaceTreeControl::HitTest","_shell_INameSpaceTreeControl_HitTest","shell.INameSpaceTreeControl_HitTest","shobjidl_core/INameSpaceTreeControl::HitTest"]
old-location: shell\INameSpaceTreeControl_HitTest.htm
tech.root: shell
ms.assetid: 2287772d-2c06-4d4b-a11e-727dd5de5326
ms.date: 12/05/2018
ms.keywords: HitTest, HitTest method [Windows Shell], HitTest method [Windows Shell],INameSpaceTreeControl interface, INameSpaceTreeControl interface [Windows Shell],HitTest method, INameSpaceTreeControl.HitTest, INameSpaceTreeControl::HitTest, _shell_INameSpaceTreeControl_HitTest, shell.INameSpaceTreeControl_HitTest, shobjidl_core/INameSpaceTreeControl::HitTest
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
 - INameSpaceTreeControl::HitTest
 - shobjidl_core/INameSpaceTreeControl::HitTest
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
 - INameSpaceTreeControl.HitTest
---

# INameSpaceTreeControl::HitTest


## -description

Retrieves the item that a given point is in, if any.

## -parameters

### -param ppt [in]

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a>*</b>

A pointer to the point to be tested.

### -param ppsiOut [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>**</b>

The address of a pointer to the item in which the point exists, or <b>NULL</b> if the point does not exist in an item.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function returns <b>S_FALSE</b> with a <b>NULL</b> item if the point does not exist in an item.