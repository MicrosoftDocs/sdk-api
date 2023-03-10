---
UID: NF:shobjidl.IDeskBand2.GetCompositionState
title: IDeskBand2::GetCompositionState (shobjidl.h)
description: Gets the composition state.
helpviewer_keywords: ["GetCompositionState","GetCompositionState method [Windows Shell]","GetCompositionState method [Windows Shell]","IDeskBand2 interface","IDeskBand2 interface [Windows Shell]","GetCompositionState method","IDeskBand2.GetCompositionState","IDeskBand2::GetCompositionState","_shell_IDeskBand2_GetCompositionState","shell.IDeskBand2_GetCompositionState","shobjidl/IDeskBand2::GetCompositionState"]
old-location: shell\IDeskBand2_GetCompositionState.htm
tech.root: shell
ms.assetid: 77c9203b-39a1-4923-a5df-68861e19e9f1
ms.date: 12/05/2018
ms.keywords: GetCompositionState, GetCompositionState method [Windows Shell], GetCompositionState method [Windows Shell],IDeskBand2 interface, IDeskBand2 interface [Windows Shell],GetCompositionState method, IDeskBand2.GetCompositionState, IDeskBand2::GetCompositionState, _shell_IDeskBand2_GetCompositionState, shell.IDeskBand2_GetCompositionState, shobjidl/IDeskBand2::GetCompositionState
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
 - IDeskBand2::GetCompositionState
 - shobjidl/IDeskBand2::GetCompositionState
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
 - IDeskBand2.GetCompositionState
---

# IDeskBand2::GetCompositionState


## -description

Gets the composition state.
<div class="alert"><b>Important</b>  You should use <a href="/windows/desktop/shell/taskbar-extensions">thumbnail toolbars</a> in new development in place of desk bands, which are not supported as of Windows 7.</div><div> </div>

## -parameters

### -param pfCompositionEnabled [out]

Type: <b>BOOL*</b>

When this method returns, contains a <b>BOOL</b> that indicates state.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.