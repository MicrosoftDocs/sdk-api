---
UID: NF:shobjidl.IDeskBand2.GetCompositionState
title: IDeskBand2::GetCompositionState
author: windows-sdk-content
description: Gets the composition state.
old-location: shell\IDeskBand2_GetCompositionState.htm
tech.root: shell
ms.assetid: 77c9203b-39a1-4923-a5df-68861e19e9f1
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetCompositionState, GetCompositionState method [Windows Shell], GetCompositionState method [Windows Shell],IDeskBand2 interface, IDeskBand2 interface [Windows Shell],GetCompositionState method, IDeskBand2.GetCompositionState, IDeskBand2::GetCompositionState, _shell_IDeskBand2_GetCompositionState, shell.IDeskBand2_GetCompositionState, shobjidl/IDeskBand2::GetCompositionState
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
 - IDeskBand2.GetCompositionState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- shobjidl.h
: 
- IDeskBand2.GetCompositionState
: 
---

# IDeskBand2::GetCompositionState


## -description


Gets the composition state.
<div class="alert"><b>Important</b>  You should use <a href="https://msdn.microsoft.com/cbf2b07d-d67c-4755-888c-d40692d13cae">thumbnail toolbars</a> in new development in place of desk bands, which are not supported as of Windows 7.</div><div> </div>

## -parameters




### -param pfCompositionEnabled [out]

Type: <b>BOOL*</b>

When this method returns, contains a <b>BOOL</b> that indicates state.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



