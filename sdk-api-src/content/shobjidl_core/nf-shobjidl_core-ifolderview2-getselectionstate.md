---
UID: NF:shobjidl_core.IFolderView2.GetSelectionState
title: IFolderView2::GetSelectionState (shobjidl_core.h)
description: Gets the selection state including check state.
helpviewer_keywords: ["GetSelectionState","GetSelectionState method [Windows Shell]","GetSelectionState method [Windows Shell]","IFolderView2 interface","IFolderView2 interface [Windows Shell]","GetSelectionState method","IFolderView2.GetSelectionState","IFolderView2::GetSelectionState","_shell_IFolderView2_GetSelectionState","shell.IFolderView2_GetSelectionState","shobjidl_core/IFolderView2::GetSelectionState"]
old-location: shell\IFolderView2_GetSelectionState.htm
tech.root: shell
ms.assetid: fc446188-c7f8-4158-a5b4-631fb374e0c4
ms.date: 12/05/2018
ms.keywords: GetSelectionState, GetSelectionState method [Windows Shell], GetSelectionState method [Windows Shell],IFolderView2 interface, IFolderView2 interface [Windows Shell],GetSelectionState method, IFolderView2.GetSelectionState, IFolderView2::GetSelectionState, _shell_IFolderView2_GetSelectionState, shell.IFolderView2_GetSelectionState, shobjidl_core/IFolderView2::GetSelectionState
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
 - IFolderView2::GetSelectionState
 - shobjidl_core/IFolderView2::GetSelectionState
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
 - IFolderView2.GetSelectionState
---

# IFolderView2::GetSelectionState


## -description

Gets the selection state including check state.

## -parameters

### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

A PIDL of the item.

### -param pdwFlags [out]

Type: <b>DWORD*</b>

Zero or one of the following <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_svsif">_SVSIF</a> constants that specify the current type of selection: <b>SVSI_FOCUSED</b>, <b>SVSI_SELECT</b>, <b>SVSI_CHECK</b>, or <b>SVSI_CHECK2</b>. Other <b>_SVSIF</b> constants are not returned by this API.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

