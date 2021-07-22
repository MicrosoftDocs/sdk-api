---
UID: NF:shobjidl.INameSpaceTreeControlEvents.OnBeginLabelEdit
title: INameSpaceTreeControlEvents::OnBeginLabelEdit (shobjidl.h)
description: Called before the IShellItem goes into edit mode.
helpviewer_keywords: ["INameSpaceTreeControlEvents interface [Windows Shell]","OnBeginLabelEdit method","INameSpaceTreeControlEvents.OnBeginLabelEdit","INameSpaceTreeControlEvents::OnBeginLabelEdit","OnBeginLabelEdit","OnBeginLabelEdit method [Windows Shell]","OnBeginLabelEdit method [Windows Shell]","INameSpaceTreeControlEvents interface","_shell_INameSpaceTreeControlEvents_OnBeginLabelEdit","shell.INameSpaceTreeControlEvents_OnBeginLabelEdit","shobjidl/INameSpaceTreeControlEvents::OnBeginLabelEdit"]
old-location: shell\INameSpaceTreeControlEvents_OnBeginLabelEdit.htm
tech.root: shell
ms.assetid: cf97e4e9-cd4c-48c0-8230-2152c9767ef2
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControlEvents interface [Windows Shell],OnBeginLabelEdit method, INameSpaceTreeControlEvents.OnBeginLabelEdit, INameSpaceTreeControlEvents::OnBeginLabelEdit, OnBeginLabelEdit, OnBeginLabelEdit method [Windows Shell], OnBeginLabelEdit method [Windows Shell],INameSpaceTreeControlEvents interface, _shell_INameSpaceTreeControlEvents_OnBeginLabelEdit, shell.INameSpaceTreeControlEvents_OnBeginLabelEdit, shobjidl/INameSpaceTreeControlEvents::OnBeginLabelEdit
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
 - INameSpaceTreeControlEvents::OnBeginLabelEdit
 - shobjidl/INameSpaceTreeControlEvents::OnBeginLabelEdit
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
 - INameSpaceTreeControlEvents.OnBeginLabelEdit
---

# INameSpaceTreeControlEvents::OnBeginLabelEdit


## -description

Called before the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> goes into edit mode.

## -parameters

### -param psi [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

Pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> for which the text is to be edited.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If this method fails, the transition to edit mode is not canceled.

## -see-also

<a href="/windows/desktop/api/shobjidl/nn-shobjidl-inamespacetreecontrolevents">INameSpaceTreeControlEvents</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>