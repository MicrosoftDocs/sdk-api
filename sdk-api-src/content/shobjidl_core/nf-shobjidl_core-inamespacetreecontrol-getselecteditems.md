---
UID: NF:shobjidl_core.INameSpaceTreeControl.GetSelectedItems
title: INameSpaceTreeControl::GetSelectedItems (shobjidl_core.h)
description: Gets an array of selected Shell items.
old-location: shell\INameSpaceTreeControl_GetSelectedItems.htm
tech.root: shell
ms.assetid: dfc81922-883a-4749-94be-3630853e38c1
ms.date: 12/05/2018
ms.keywords: GetSelectedItems, GetSelectedItems method [Windows Shell], GetSelectedItems method [Windows Shell],INameSpaceTreeControl interface, INameSpaceTreeControl interface [Windows Shell],GetSelectedItems method, INameSpaceTreeControl.GetSelectedItems, INameSpaceTreeControl::GetSelectedItems, _shell_INameSpaceTreeControl_GetSelectedItems, shell.INameSpaceTreeControl_GetSelectedItems, shobjidl_core/INameSpaceTreeControl::GetSelectedItems
ms.topic: method
f1_keywords:
- shobjidl_core/INameSpaceTreeControl.GetSelectedItems
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
- INameSpaceTreeControl.GetSelectedItems
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INameSpaceTreeControl::GetSelectedItems


## -description


Gets an array of selected Shell items.


## -parameters




### -param psiaItems [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>**</b>

A pointer to an array of selected Shell items.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



