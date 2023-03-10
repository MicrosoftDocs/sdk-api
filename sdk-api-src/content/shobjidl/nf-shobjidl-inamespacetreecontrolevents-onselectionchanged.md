---
UID: NF:shobjidl.INameSpaceTreeControlEvents.OnSelectionChanged
title: INameSpaceTreeControlEvents::OnSelectionChanged (shobjidl.h)
description: Called when the selection changes.
helpviewer_keywords: ["INameSpaceTreeControlEvents interface [Windows Shell]","OnSelectionChanged method","INameSpaceTreeControlEvents.OnSelectionChanged","INameSpaceTreeControlEvents::OnSelectionChanged","OnSelectionChanged","OnSelectionChanged method [Windows Shell]","OnSelectionChanged method [Windows Shell]","INameSpaceTreeControlEvents interface","_shell_INameSpaceTreeControlEvents_OnSelectionChanged","shell.INameSpaceTreeControlEvents_OnSelectionChanged","shobjidl/INameSpaceTreeControlEvents::OnSelectionChanged"]
old-location: shell\INameSpaceTreeControlEvents_OnSelectionChanged.htm
tech.root: shell
ms.assetid: ecc84586-ec37-4ece-a890-6adfc7a94ad6
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControlEvents interface [Windows Shell],OnSelectionChanged method, INameSpaceTreeControlEvents.OnSelectionChanged, INameSpaceTreeControlEvents::OnSelectionChanged, OnSelectionChanged, OnSelectionChanged method [Windows Shell], OnSelectionChanged method [Windows Shell],INameSpaceTreeControlEvents interface, _shell_INameSpaceTreeControlEvents_OnSelectionChanged, shell.INameSpaceTreeControlEvents_OnSelectionChanged, shobjidl/INameSpaceTreeControlEvents::OnSelectionChanged
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
 - INameSpaceTreeControlEvents::OnSelectionChanged
 - shobjidl/INameSpaceTreeControlEvents::OnSelectionChanged
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
 - INameSpaceTreeControlEvents.OnSelectionChanged
---

# INameSpaceTreeControlEvents::OnSelectionChanged


## -description

Called when the selection changes.

## -parameters

### -param psiaSelection [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>*</b>

An array of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> objects that contains the new selection.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl/nn-shobjidl-inamespacetreecontrolevents">INameSpaceTreeControlEvents</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>