---
UID: NF:shobjidl.INameSpaceTreeControlEvents.OnAfterContextMenu
title: INameSpaceTreeControlEvents::OnAfterContextMenu (shobjidl.h)
description: Called after a context menu is displayed.
helpviewer_keywords: ["INameSpaceTreeControlEvents interface [Windows Shell]","OnAfterContextMenu method","INameSpaceTreeControlEvents.OnAfterContextMenu","INameSpaceTreeControlEvents::OnAfterContextMenu","OnAfterContextMenu","OnAfterContextMenu method [Windows Shell]","OnAfterContextMenu method [Windows Shell]","INameSpaceTreeControlEvents interface","_shell_INameSpaceTreeControlEvents_OnAfterContextMenu","shell.INameSpaceTreeControlEvents_OnAfterContextMenu","shobjidl/INameSpaceTreeControlEvents::OnAfterContextMenu"]
old-location: shell\INameSpaceTreeControlEvents_OnAfterContextMenu.htm
tech.root: shell
ms.assetid: 6d562938-9816-4df9-b5b6-0ed52b1e4835
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControlEvents interface [Windows Shell],OnAfterContextMenu method, INameSpaceTreeControlEvents.OnAfterContextMenu, INameSpaceTreeControlEvents::OnAfterContextMenu, OnAfterContextMenu, OnAfterContextMenu method [Windows Shell], OnAfterContextMenu method [Windows Shell],INameSpaceTreeControlEvents interface, _shell_INameSpaceTreeControlEvents_OnAfterContextMenu, shell.INameSpaceTreeControlEvents_OnAfterContextMenu, shobjidl/INameSpaceTreeControlEvents::OnAfterContextMenu
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
 - INameSpaceTreeControlEvents::OnAfterContextMenu
 - shobjidl/INameSpaceTreeControlEvents::OnAfterContextMenu
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
 - INameSpaceTreeControlEvents.OnAfterContextMenu
---

# INameSpaceTreeControlEvents::OnAfterContextMenu


## -description

Called after a context menu is displayed.

## -parameters

### -param psi [in, optional]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> from which the context menu is generated. This value can be <b>NULL</b> only if the <a href="/windows/desktop/api/shobjidl/ne-shobjidl-nstcstyle2">NSTCS2_SHOWNULLSPACEMENU</a> flag is set.

### -param pcmIn [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu">IContextMenu</a>*</b>

A pointer to the context menu.

### -param riid [in]

Type: <b>REFIID</b>

Reference to the IID of the context menu.

### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the address of a pointer to the interface specified in <i>riid</i>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method allows client to completely replace the context menu. This method will allow the client to use the context menu returned by <i>ppv</i> and not necessarily the one specified in <i>pcmIn</i>.

## -see-also

<a href="/windows/desktop/api/shobjidl/nn-shobjidl-inamespacetreecontrolevents">INameSpaceTreeControlEvents</a>



<a href="/windows/desktop/api/shobjidl/ne-shobjidl-nstcstyle2">NSTCSTYLE2</a>