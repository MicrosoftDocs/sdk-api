---
UID: NF:shobjidl.INameSpaceTreeControlEvents.OnItemAdded
title: INameSpaceTreeControlEvents::OnItemAdded (shobjidl.h)
description: Called after an IShellItem has been added.
helpviewer_keywords: ["INameSpaceTreeControlEvents interface [Windows Shell]","OnItemAdded method","INameSpaceTreeControlEvents.OnItemAdded","INameSpaceTreeControlEvents::OnItemAdded","OnItemAdded","OnItemAdded method [Windows Shell]","OnItemAdded method [Windows Shell]","INameSpaceTreeControlEvents interface","_shell_INameSpaceTreeControlEvents_OnItemAdded","shell.INameSpaceTreeControlEvents_OnItemAdded","shobjidl/INameSpaceTreeControlEvents::OnItemAdded"]
old-location: shell\INameSpaceTreeControlEvents_OnItemAdded.htm
tech.root: shell
ms.assetid: 7737e014-8e46-43da-b017-133bbf12b433
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControlEvents interface [Windows Shell],OnItemAdded method, INameSpaceTreeControlEvents.OnItemAdded, INameSpaceTreeControlEvents::OnItemAdded, OnItemAdded, OnItemAdded method [Windows Shell], OnItemAdded method [Windows Shell],INameSpaceTreeControlEvents interface, _shell_INameSpaceTreeControlEvents_OnItemAdded, shell.INameSpaceTreeControlEvents_OnItemAdded, shobjidl/INameSpaceTreeControlEvents::OnItemAdded
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
 - INameSpaceTreeControlEvents::OnItemAdded
 - shobjidl/INameSpaceTreeControlEvents::OnItemAdded
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
 - INameSpaceTreeControlEvents.OnItemAdded
---

# INameSpaceTreeControlEvents::OnItemAdded


## -description

Called after an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> has been added.

## -parameters

### -param psi [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that was added.

### -param fIsRoot [in]

Type: <b>BOOL</b>

Specifies whether the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that was added is a root.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl/nn-shobjidl-inamespacetreecontrolevents">INameSpaceTreeControlEvents</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>