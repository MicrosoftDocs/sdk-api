---
UID: NF:shobjidl_core.INameSpaceTreeControl.GetRootItems
title: INameSpaceTreeControl::GetRootItems (shobjidl_core.h)
author: windows-sdk-content
description: Gets an array of the root items.
old-location: shell\INameSpaceTreeControl_GetRootItems.htm
tech.root: shell
ms.assetid: ca957f8c-ac8e-472e-b762-ddc45e20462d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetRootItems, GetRootItems method [Windows Shell], GetRootItems method [Windows Shell],INameSpaceTreeControl interface, INameSpaceTreeControl interface [Windows Shell],GetRootItems method, INameSpaceTreeControl.GetRootItems, INameSpaceTreeControl::GetRootItems, _shell_INameSpaceTreeControl_GetRootItems, shell.INameSpaceTreeControl_GetRootItems, shobjidl_core/INameSpaceTreeControl::GetRootItems
ms.topic: method
f1_keywords: 
 - "shobjidl_core/INameSpaceTreeControl.GetRootItems"
dev_langs:
 - c++
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
 - INameSpaceTreeControl.GetRootItems
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INameSpaceTreeControl::GetRootItems


## -description


Gets an array of the root items.


## -parameters




### -param ppsiaRootItems [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>**</b>

A pointer to an array of root items.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



