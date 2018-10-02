---
UID: NF:shobjidl.IDeskBand2.SetCompositionState
title: IDeskBand2::SetCompositionState
author: windows-sdk-content
description: Sets the composition state.
old-location: shell\IDeskBand2_SetCompositionState.htm
tech.root: Shell
ms.assetid: 183cc6fa-4dc4-4272-8d61-a0a426aeefda
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IDeskBand2 interface [Windows Shell],SetCompositionState method, IDeskBand2.SetCompositionState, IDeskBand2::SetCompositionState, SetCompositionState, SetCompositionState method [Windows Shell], SetCompositionState method [Windows Shell],IDeskBand2 interface, _shell_IDeskBand2_SetCompositionState, shell.IDeskBand2_SetCompositionState, shobjidl/IDeskBand2::SetCompositionState
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IDeskBand2.SetCompositionState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDeskBand2::SetCompositionState


## -description


Sets the composition state.
<div class="alert"><b>Important</b>  You should use <a href="https://msdn.microsoft.com/cbf2b07d-d67c-4755-888c-d40692d13cae">thumbnail toolbars</a> in new development in place of desk bands, which are not supported as of Windows 7.</div><div> </div>

## -parameters




### -param fCompositionEnabled [in]

Type: <b>BOOL</b>

<b>TRUE</b> to enable the composition state; otherwise, <b>FALSE</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



