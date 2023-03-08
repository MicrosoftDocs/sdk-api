---
UID: NF:shobjidl.IDeskBand2.SetCompositionState
title: IDeskBand2::SetCompositionState (shobjidl.h)
description: Sets the composition state.
helpviewer_keywords: ["IDeskBand2 interface [Windows Shell]","SetCompositionState method","IDeskBand2.SetCompositionState","IDeskBand2::SetCompositionState","SetCompositionState","SetCompositionState method [Windows Shell]","SetCompositionState method [Windows Shell]","IDeskBand2 interface","_shell_IDeskBand2_SetCompositionState","shell.IDeskBand2_SetCompositionState","shobjidl/IDeskBand2::SetCompositionState"]
old-location: shell\IDeskBand2_SetCompositionState.htm
tech.root: shell
ms.assetid: 183cc6fa-4dc4-4272-8d61-a0a426aeefda
ms.date: 12/05/2018
ms.keywords: IDeskBand2 interface [Windows Shell],SetCompositionState method, IDeskBand2.SetCompositionState, IDeskBand2::SetCompositionState, SetCompositionState, SetCompositionState method [Windows Shell], SetCompositionState method [Windows Shell],IDeskBand2 interface, _shell_IDeskBand2_SetCompositionState, shell.IDeskBand2_SetCompositionState, shobjidl/IDeskBand2::SetCompositionState
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
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDeskBand2::SetCompositionState
 - shobjidl/IDeskBand2::SetCompositionState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IDeskBand2.SetCompositionState
---

# IDeskBand2::SetCompositionState


## -description

Sets the composition state.
<div class="alert"><b>Important</b>  You should use <a href="/windows/desktop/shell/taskbar-extensions">thumbnail toolbars</a> in new development in place of desk bands, which are not supported as of Windows 7.</div><div> </div>

## -parameters

### -param fCompositionEnabled [in]

Type: <b>BOOL</b>

<b>TRUE</b> to enable the composition state; otherwise, <b>FALSE</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.