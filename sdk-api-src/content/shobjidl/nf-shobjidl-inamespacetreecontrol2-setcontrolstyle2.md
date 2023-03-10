---
UID: NF:shobjidl.INameSpaceTreeControl2.SetControlStyle2
title: INameSpaceTreeControl2::SetControlStyle2 (shobjidl.h)
description: Sets the extended display styles for the namespace object's treeview controls.
helpviewer_keywords: ["INameSpaceTreeControl2 interface [Windows Shell]","SetControlStyle2 method","INameSpaceTreeControl2.SetControlStyle2","INameSpaceTreeControl2::SetControlStyle2","SetControlStyle2","SetControlStyle2 method [Windows Shell]","SetControlStyle2 method [Windows Shell]","INameSpaceTreeControl2 interface","_shell_INameSpaceTreeControl2_SetControlStyle2","shell.INameSpaceTreeControl2_SetControlStyle2","shobjidl/INameSpaceTreeControl2::SetControlStyle2"]
old-location: shell\INameSpaceTreeControl2_SetControlStyle2.htm
tech.root: shell
ms.assetid: 17d54fa9-ff5c-4fca-a7a6-7ecd4a58c7b9
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControl2 interface [Windows Shell],SetControlStyle2 method, INameSpaceTreeControl2.SetControlStyle2, INameSpaceTreeControl2::SetControlStyle2, SetControlStyle2, SetControlStyle2 method [Windows Shell], SetControlStyle2 method [Windows Shell],INameSpaceTreeControl2 interface, _shell_INameSpaceTreeControl2_SetControlStyle2, shell.INameSpaceTreeControl2_SetControlStyle2, shobjidl/INameSpaceTreeControl2::SetControlStyle2
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
 - INameSpaceTreeControl2::SetControlStyle2
 - shobjidl/INameSpaceTreeControl2::SetControlStyle2
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
 - INameSpaceTreeControl2.SetControlStyle2
---

# INameSpaceTreeControl2::SetControlStyle2


## -description

Sets the extended display styles for the namespace object's treeview controls.

## -parameters

### -param nstcsMask [in]

Type: <b><a href="/windows/desktop/api/shobjidl/ne-shobjidl-nstcstyle2">NSTCSTYLE2</a></b>

One or more of the <a href="/windows/desktop/api/shobjidl/ne-shobjidl-nstcstyle2">NSTCSTYLE2</a> constants that specify the styles for which the method should set new values.

### -param nstcsStyle [in]

Type: <b><a href="/windows/desktop/api/shobjidl/ne-shobjidl-nstcstyle2">NSTCSTYLE2</a></b>

A bitmap that contains the new values for the styles specified in <i>nstcsMask</i>. If the bit that represents the individual <a href="/windows/desktop/api/shobjidl/ne-shobjidl-nstcstyle2">NSTCSTYLE2</a> value is 0, that style is not used. If the value is 1, the style is applied to the treeview. Styles in positions not specified in <i>nstcsMask</i> are left at their current setting regardless of their bit's value in this bitmap.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl/nn-shobjidl-inamespacetreecontrol2">INameSpaceTreeControl2</a>



<a href="/windows/desktop/api/shobjidl/nf-shobjidl-inamespacetreecontrol2-getcontrolstyle2">INameSpaceTreeControl2::GetControlStyle2</a>



<a href="/windows/desktop/api/shobjidl/nf-shobjidl-inamespacetreecontrol2-setcontrolstyle">INameSpaceTreeControl2::SetControlStyle</a>



<a href="/windows/desktop/api/shobjidl/ne-shobjidl-nstcstyle2">NSTCSTYLE2</a>