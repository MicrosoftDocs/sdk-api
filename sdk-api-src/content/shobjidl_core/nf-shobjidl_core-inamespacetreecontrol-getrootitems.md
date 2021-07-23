---
UID: NF:shobjidl_core.INameSpaceTreeControl.GetRootItems
title: INameSpaceTreeControl::GetRootItems (shobjidl_core.h)
description: Gets an array of the root items.
helpviewer_keywords: ["GetRootItems","GetRootItems method [Windows Shell]","GetRootItems method [Windows Shell]","INameSpaceTreeControl interface","INameSpaceTreeControl interface [Windows Shell]","GetRootItems method","INameSpaceTreeControl.GetRootItems","INameSpaceTreeControl::GetRootItems","_shell_INameSpaceTreeControl_GetRootItems","shell.INameSpaceTreeControl_GetRootItems","shobjidl_core/INameSpaceTreeControl::GetRootItems"]
old-location: shell\INameSpaceTreeControl_GetRootItems.htm
tech.root: shell
ms.assetid: ca957f8c-ac8e-472e-b762-ddc45e20462d
ms.date: 12/05/2018
ms.keywords: GetRootItems, GetRootItems method [Windows Shell], GetRootItems method [Windows Shell],INameSpaceTreeControl interface, INameSpaceTreeControl interface [Windows Shell],GetRootItems method, INameSpaceTreeControl.GetRootItems, INameSpaceTreeControl::GetRootItems, _shell_INameSpaceTreeControl_GetRootItems, shell.INameSpaceTreeControl_GetRootItems, shobjidl_core/INameSpaceTreeControl::GetRootItems
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
 - INameSpaceTreeControl::GetRootItems
 - shobjidl_core/INameSpaceTreeControl::GetRootItems
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
 - INameSpaceTreeControl.GetRootItems
---

# INameSpaceTreeControl::GetRootItems


## -description

Gets an array of the root items.

## -parameters

### -param ppsiaRootItems [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>**</b>

A pointer to an array of root items.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.