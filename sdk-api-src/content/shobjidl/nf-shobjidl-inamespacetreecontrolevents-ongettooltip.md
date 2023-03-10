---
UID: NF:shobjidl.INameSpaceTreeControlEvents.OnGetToolTip
title: INameSpaceTreeControlEvents::OnGetToolTip (shobjidl.h)
description: Enables you to provide a tooltip.
helpviewer_keywords: ["INameSpaceTreeControlEvents interface [Windows Shell]","OnGetToolTip method","INameSpaceTreeControlEvents.OnGetToolTip","INameSpaceTreeControlEvents::OnGetToolTip","OnGetToolTip","OnGetToolTip method [Windows Shell]","OnGetToolTip method [Windows Shell]","INameSpaceTreeControlEvents interface","_shell_INameSpaceTreeControlEvents_OnGetToolTip","shell.INameSpaceTreeControlEvents_OnGetToolTip","shobjidl/INameSpaceTreeControlEvents::OnGetToolTip"]
old-location: shell\INameSpaceTreeControlEvents_OnGetToolTip.htm
tech.root: shell
ms.assetid: 57970b8d-2461-43af-8959-c51f27679407
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControlEvents interface [Windows Shell],OnGetToolTip method, INameSpaceTreeControlEvents.OnGetToolTip, INameSpaceTreeControlEvents::OnGetToolTip, OnGetToolTip, OnGetToolTip method [Windows Shell], OnGetToolTip method [Windows Shell],INameSpaceTreeControlEvents interface, _shell_INameSpaceTreeControlEvents_OnGetToolTip, shell.INameSpaceTreeControlEvents_OnGetToolTip, shobjidl/INameSpaceTreeControlEvents::OnGetToolTip
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
 - INameSpaceTreeControlEvents::OnGetToolTip
 - shobjidl/INameSpaceTreeControlEvents::OnGetToolTip
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
 - INameSpaceTreeControlEvents.OnGetToolTip
---

# INameSpaceTreeControlEvents::OnGetToolTip


## -description

Enables you to provide a tooltip.

## -parameters

### -param psi [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

Pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that contains the tooltip.

### -param pszTip [out]

Type: <b>LPWSTR</b>

When this method returns, contains the text of the tooltip.

### -param cchTip [in]

Type: <b>int</b>

The size of the tooltip in characters.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If this method returns S_OK, the client provides its own tooltip. Otherwise the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol">INameSpaceTreeControl</a> will extract one.

## -see-also

<a href="/windows/desktop/api/shobjidl/nn-shobjidl-inamespacetreecontrolevents">INameSpaceTreeControlEvents</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>