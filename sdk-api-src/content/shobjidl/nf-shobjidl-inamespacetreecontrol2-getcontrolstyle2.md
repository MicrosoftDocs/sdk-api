---
UID: NF:shobjidl.INameSpaceTreeControl2.GetControlStyle2
title: INameSpaceTreeControl2::GetControlStyle2 (shobjidl.h)
description: Gets the extended display styles set for the namespace object's treeview controls.
helpviewer_keywords: ["GetControlStyle2","GetControlStyle2 method [Windows Shell]","GetControlStyle2 method [Windows Shell]","INameSpaceTreeControl2 interface","INameSpaceTreeControl2 interface [Windows Shell]","GetControlStyle2 method","INameSpaceTreeControl2.GetControlStyle2","INameSpaceTreeControl2::GetControlStyle2","_shell_INameSpaceTreeControl2_GetControlStyle2","shell.INameSpaceTreeControl2_GetControlStyle2","shobjidl/INameSpaceTreeControl2::GetControlStyle2"]
old-location: shell\INameSpaceTreeControl2_GetControlStyle2.htm
tech.root: shell
ms.assetid: 1c96d936-2a79-491b-8e1e-2dd0e71aba10
ms.date: 12/05/2018
ms.keywords: GetControlStyle2, GetControlStyle2 method [Windows Shell], GetControlStyle2 method [Windows Shell],INameSpaceTreeControl2 interface, INameSpaceTreeControl2 interface [Windows Shell],GetControlStyle2 method, INameSpaceTreeControl2.GetControlStyle2, INameSpaceTreeControl2::GetControlStyle2, _shell_INameSpaceTreeControl2_GetControlStyle2, shell.INameSpaceTreeControl2_GetControlStyle2, shobjidl/INameSpaceTreeControl2::GetControlStyle2
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - INameSpaceTreeControl2::GetControlStyle2
 - shobjidl/INameSpaceTreeControl2::GetControlStyle2
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
 - INameSpaceTreeControl2.GetControlStyle2
---

# INameSpaceTreeControl2::GetControlStyle2


## -description

Gets the extended display styles set for the namespace object's treeview controls.

## -parameters

### -param nstcsMask [in]

Type: <b><a href="/windows/desktop/api/shobjidl/ne-shobjidl-nstcstyle2">NSTCSTYLE2</a></b>

One or more of the <a href="/windows/desktop/api/shobjidl/ne-shobjidl-nstcstyle2">NSTCSTYLE2</a> constants that specify the values for which the method should retrieve the current settings.

### -param pnstcsStyle [out]

Type: <b><a href="/windows/desktop/api/shobjidl/ne-shobjidl-nstcstyle2">NSTCSTYLE2</a>*</b>

Pointer to a value that, when this method returns successfully, receives the values requested in <i>nstcsMask</i>. If the bit that represents the individual <a href="/windows/desktop/api/shobjidl/ne-shobjidl-nstcstyle2">NSTCSTYLE2</a> value is 0, that value is not set. If the value is 1, it is the current setting. Bit values in positions not specifically requested in <i>nstcsMask</i> do not necessarily reflect the current settings and should not be used.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl/nn-shobjidl-inamespacetreecontrol2">INameSpaceTreeControl2</a>



<a href="/windows/desktop/api/shobjidl/nf-shobjidl-inamespacetreecontrol2-getcontrolstyle">INameSpaceTreeControl2::GetControlStyle</a>



<a href="/windows/desktop/api/shobjidl/nf-shobjidl-inamespacetreecontrol2-setcontrolstyle2">INameSpaceTreeControl2::SetControlStyle2</a>



<a href="/windows/desktop/api/shobjidl/ne-shobjidl-nstcstyle2">NSTCSTYLE2</a>