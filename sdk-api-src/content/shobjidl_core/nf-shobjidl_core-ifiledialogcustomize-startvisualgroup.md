---
UID: NF:shobjidl_core.IFileDialogCustomize.StartVisualGroup
title: IFileDialogCustomize::StartVisualGroup (shobjidl_core.h)
description: Declares a visual group in the dialog. Subsequent calls to any &quot;add&quot; method add those elements to this group.
helpviewer_keywords: ["IFileDialogCustomize interface [Windows Shell]","StartVisualGroup method","IFileDialogCustomize.StartVisualGroup","IFileDialogCustomize::StartVisualGroup","StartVisualGroup","StartVisualGroup method [Windows Shell]","StartVisualGroup method [Windows Shell]","IFileDialogCustomize interface","shell.IFileDialogCustomize_StartVisualGroup","shell_IFileDialogCustomize_StartVisualGroup","shobjidl_core/IFileDialogCustomize::StartVisualGroup"]
old-location: shell\IFileDialogCustomize_StartVisualGroup.htm
tech.root: shell
ms.assetid: 2626c820-3731-474d-9ddb-d2a8966c3d35
ms.date: 12/05/2018
ms.keywords: IFileDialogCustomize interface [Windows Shell],StartVisualGroup method, IFileDialogCustomize.StartVisualGroup, IFileDialogCustomize::StartVisualGroup, StartVisualGroup, StartVisualGroup method [Windows Shell], StartVisualGroup method [Windows Shell],IFileDialogCustomize interface, shell.IFileDialogCustomize_StartVisualGroup, shell_IFileDialogCustomize_StartVisualGroup, shobjidl_core/IFileDialogCustomize::StartVisualGroup
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
 - IFileDialogCustomize::StartVisualGroup
 - shobjidl_core/IFileDialogCustomize::StartVisualGroup
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
 - IFileDialogCustomize.StartVisualGroup
---

# IFileDialogCustomize::StartVisualGroup


## -description

Declares a visual group in the dialog. Subsequent calls to any "add" method add those elements to this group.

## -parameters

### -param dwIDCtl [in]

Type: <b>DWORD</b>

The ID of the visual group.

### -param pszLabel [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer that contains text, as a null-terminated Unicode string, that appears next to the visual group.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Controls will continue to be added to this visual group until you call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogcustomize-endvisualgroup">IFileDialogCustomize::EndVisualGroup</a>.
              

A visual group can be hidden and disabled like any other control, except that doing so affects all of the controls within it. Individual members of the visual group can also be hidden and disabled singly.