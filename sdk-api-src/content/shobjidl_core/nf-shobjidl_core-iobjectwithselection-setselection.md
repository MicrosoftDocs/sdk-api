---
UID: NF:shobjidl_core.IObjectWithSelection.SetSelection
title: IObjectWithSelection::SetSelection (shobjidl_core.h)
description: Provides the Shell item array that specifies the items included in the selection.
helpviewer_keywords: ["IObjectWithSelection interface [Windows Shell]","SetSelection method","IObjectWithSelection.SetSelection","IObjectWithSelection::SetSelection","SetSelection","SetSelection method [Windows Shell]","SetSelection method [Windows Shell]","IObjectWithSelection interface","_shell_IObjectWithSelection_SetSelection","shell.IObjectWithSelection_SetSelection","shobjidl_core/IObjectWithSelection::SetSelection"]
old-location: shell\IObjectWithSelection_SetSelection.htm
tech.root: shell
ms.assetid: e561b8f8-36e9-45ec-beb2-62d7f429dec4
ms.date: 12/05/2018
ms.keywords: IObjectWithSelection interface [Windows Shell],SetSelection method, IObjectWithSelection.SetSelection, IObjectWithSelection::SetSelection, SetSelection, SetSelection method [Windows Shell], SetSelection method [Windows Shell],IObjectWithSelection interface, _shell_IObjectWithSelection_SetSelection, shell.IObjectWithSelection_SetSelection, shobjidl_core/IObjectWithSelection::SetSelection
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
 - IObjectWithSelection::SetSelection
 - shobjidl_core/IObjectWithSelection::SetSelection
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
 - IObjectWithSelection.SetSelection
---

# IObjectWithSelection::SetSelection


## -description

Provides the Shell item array that specifies the items included in the selection.

## -parameters

### -param psia [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>*</b>

A pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a> that represents the selected items.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.