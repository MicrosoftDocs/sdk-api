---
UID: NF:shobjidl.INameSpaceTreeControlEvents.OnEndLabelEdit
title: INameSpaceTreeControlEvents::OnEndLabelEdit (shobjidl.h)
description: Called after the IShellItem leaves edit mode.
helpviewer_keywords: ["INameSpaceTreeControlEvents interface [Windows Shell]","OnEndLabelEdit method","INameSpaceTreeControlEvents.OnEndLabelEdit","INameSpaceTreeControlEvents::OnEndLabelEdit","OnEndLabelEdit","OnEndLabelEdit method [Windows Shell]","OnEndLabelEdit method [Windows Shell]","INameSpaceTreeControlEvents interface","_shell_INameSpaceTreeControlEvents_OnEndLabelEdit","shell.INameSpaceTreeControlEvents_OnEndLabelEdit","shobjidl/INameSpaceTreeControlEvents::OnEndLabelEdit"]
old-location: shell\INameSpaceTreeControlEvents_OnEndLabelEdit.htm
tech.root: shell
ms.assetid: deeb1cc7-e943-47bd-82f0-089fb3f4c3c6
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControlEvents interface [Windows Shell],OnEndLabelEdit method, INameSpaceTreeControlEvents.OnEndLabelEdit, INameSpaceTreeControlEvents::OnEndLabelEdit, OnEndLabelEdit, OnEndLabelEdit method [Windows Shell], OnEndLabelEdit method [Windows Shell],INameSpaceTreeControlEvents interface, _shell_INameSpaceTreeControlEvents_OnEndLabelEdit, shell.INameSpaceTreeControlEvents_OnEndLabelEdit, shobjidl/INameSpaceTreeControlEvents::OnEndLabelEdit
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
 - INameSpaceTreeControlEvents::OnEndLabelEdit
 - shobjidl/INameSpaceTreeControlEvents::OnEndLabelEdit
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
 - INameSpaceTreeControlEvents.OnEndLabelEdit
---

# INameSpaceTreeControlEvents::OnEndLabelEdit


## -description

Called after the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> leaves edit mode.

## -parameters

### -param psi [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> for which the text was edited.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl/nn-shobjidl-inamespacetreecontrolevents">INameSpaceTreeControlEvents</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>