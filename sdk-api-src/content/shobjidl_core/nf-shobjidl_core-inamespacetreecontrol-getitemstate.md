---
UID: NF:shobjidl_core.INameSpaceTreeControl.GetItemState
title: INameSpaceTreeControl::GetItemState
author: windows-sdk-content
description: Gets state information about a Shell item.
old-location: shell\INameSpaceTreeControl_GetItemState.htm
tech.root: shell
ms.assetid: 78bee2db-6a28-4fcb-9c43-ab411196ab04
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: GetItemState, GetItemState method [Windows Shell], GetItemState method [Windows Shell],INameSpaceTreeControl interface, INameSpaceTreeControl interface [Windows Shell],GetItemState method, INameSpaceTreeControl.GetItemState, INameSpaceTreeControl::GetItemState, _shell_INameSpaceTreeControl_GetItemState, shell.INameSpaceTreeControl_GetItemState, shobjidl_core/INameSpaceTreeControl::GetItemState
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
 - INameSpaceTreeControl.GetItemState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INameSpaceTreeControl::GetItemState


## -description


Gets state information about a Shell item.


## -parameters




### -param psi [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to the Shell item from which to retrieve the state.


### -param nstcisMask [in]

Type: <b><a href="https://msdn.microsoft.com/1f3fd526-c044-41ff-9e05-c6d91d386b42">NSTCITEMSTATE</a></b>

Specifies which information is being requested, in the form of a bitmap. One or more of the <a href="https://msdn.microsoft.com/1f3fd526-c044-41ff-9e05-c6d91d386b42">NSTCITEMSTATE</a> constants.


### -param pnstcisFlags [out]

Type: <b><a href="https://msdn.microsoft.com/1f3fd526-c044-41ff-9e05-c6d91d386b42">NSTCITEMSTATE</a>*</b>

When this method returns, points to a bitmap that contains the values requested in <i>nstcisMask</i>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <i>nstcisMask</i> value specifies which bits in the value pointed to by <i>pnstcisFlags</i> are requested. As a simple example, if <i>nstcisMask</i>=NSTCIS_SELECTED, then only the first bit in the value pointed to by <i>pnstcisFlags</i> is valid when this method returns. If the first bit in the value pointed to by <i>pnstcisFlags</i> is 1, then the NSTCIS_SELECTED flag is set. If the first bit in the value pointed to by <i>pnstcisFlags</i> is 0, then the NSTCIS_SELECTED flag is not set.



