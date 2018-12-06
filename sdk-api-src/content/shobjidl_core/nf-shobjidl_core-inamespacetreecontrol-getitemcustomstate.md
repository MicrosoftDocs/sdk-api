---
UID: NF:shobjidl_core.INameSpaceTreeControl.GetItemCustomState
title: INameSpaceTreeControl::GetItemCustomState
author: windows-sdk-content
description: Gets the state of the checkbox associated with a given Shell item.
old-location: shell\INameSpaceTreeControl_GetItemCustomState.htm
tech.root: shell
ms.assetid: 16fb3e3a-1686-4bdf-9112-564bb85fb601
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetItemCustomState, GetItemCustomState method [Windows Shell], GetItemCustomState method [Windows Shell],INameSpaceTreeControl interface, INameSpaceTreeControl interface [Windows Shell],GetItemCustomState method, INameSpaceTreeControl.GetItemCustomState, INameSpaceTreeControl::GetItemCustomState, _shell_INameSpaceTreeControl_GetItemCustomState, shell.INameSpaceTreeControl_GetItemCustomState, shobjidl_core/INameSpaceTreeControl::GetItemCustomState
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
 - INameSpaceTreeControl.GetItemCustomState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INameSpaceTreeControl::GetItemCustomState


## -description


Gets the state of the checkbox associated with a given Shell item.


## -parameters




### -param psi [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to the Shell item for which checkbox state is being retrieved.


### -param piStateNumber [out]

Type: <b>int*</b>

A pointer to the state of the checkbox for the Shell item.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



