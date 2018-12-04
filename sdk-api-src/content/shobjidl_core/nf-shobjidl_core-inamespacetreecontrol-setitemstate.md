---
UID: NF:shobjidl_core.INameSpaceTreeControl.SetItemState
title: INameSpaceTreeControl::SetItemState
author: windows-sdk-content
description: Sets state information for a Shell item.
old-location: shell\INameSpaceTreeControl_SetItemState.htm
tech.root: shell
ms.assetid: f57c5abc-0803-409d-9938-3826f9d8058d
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: INameSpaceTreeControl interface [Windows Shell],SetItemState method, INameSpaceTreeControl.SetItemState, INameSpaceTreeControl::SetItemState, SetItemState, SetItemState method [Windows Shell], SetItemState method [Windows Shell],INameSpaceTreeControl interface, _shell_INameSpaceTreeControl_SetItemState, shell.INameSpaceTreeControl_SetItemState, shobjidl_core/INameSpaceTreeControl::SetItemState
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - INameSpaceTreeControl.SetItemState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INameSpaceTreeControl::SetItemState


## -description


Sets state information for a Shell item.


## -parameters




### -param psi [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to the Shell item for which to set the state.


### -param nstcisMask [in]

Type: <b><a href="https://msdn.microsoft.com/1f3fd526-c044-41ff-9e05-c6d91d386b42">NSTCITEMSTATE</a></b>

Specifies which information is being set, in the form of a bitmap. One or more of the <a href="https://msdn.microsoft.com/1f3fd526-c044-41ff-9e05-c6d91d386b42">NSTCITEMSTATE</a> constants.


### -param nstcisFlags [in]

Type: <b><a href="https://msdn.microsoft.com/1f3fd526-c044-41ff-9e05-c6d91d386b42">NSTCITEMSTATE</a></b>

A bitmap that contains the values to set for the flags specified in <i>nstcisMask</i>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <i>nstcisMask</i> value specifies which bits in the value pointed to by <i>pnstcisFlags</i> are to be set. Other bits are ignored. As a simple example, if <i>nstcisMask</i>=NSTCIS_SELECTED, then the first bit in the <i>nstcisFlags</i> value determines whether that flag is set (1) or removed (0).



