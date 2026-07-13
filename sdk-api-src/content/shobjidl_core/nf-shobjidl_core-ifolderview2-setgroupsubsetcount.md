---
UID: NF:shobjidl_core.IFolderView2.SetGroupSubsetCount
title: IFolderView2::SetGroupSubsetCount (shobjidl_core.h)
description: Turns on group subsetting and sets the number of visible rows of items in each group.
helpviewer_keywords: ["IFolderView2 interface [Windows Shell]","SetGroupSubsetCount method","IFolderView2.SetGroupSubsetCount","IFolderView2::SetGroupSubsetCount","SetGroupSubsetCount","SetGroupSubsetCount method [Windows Shell]","SetGroupSubsetCount method [Windows Shell]","IFolderView2 interface","_shell_IFolderView2_SetGroupSubsetCount","shell.IFolderView2_SetGroupSubsetCount","shobjidl_core/IFolderView2::SetGroupSubsetCount"]
old-location: shell\IFolderView2_SetGroupSubsetCount.htm
tech.root: shell
ms.assetid: 5aacc63a-d129-4539-a43f-f4dd74ab4fea
ms.date: 12/05/2018
ms.keywords: IFolderView2 interface [Windows Shell],SetGroupSubsetCount method, IFolderView2.SetGroupSubsetCount, IFolderView2::SetGroupSubsetCount, SetGroupSubsetCount, SetGroupSubsetCount method [Windows Shell], SetGroupSubsetCount method [Windows Shell],IFolderView2 interface, _shell_IFolderView2_SetGroupSubsetCount, shell.IFolderView2_SetGroupSubsetCount, shobjidl_core/IFolderView2::SetGroupSubsetCount
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
 - IFolderView2::SetGroupSubsetCount
 - shobjidl_core/IFolderView2::SetGroupSubsetCount
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
 - IFolderView2.SetGroupSubsetCount
---

# IFolderView2::SetGroupSubsetCount


## -description

Turns on group subsetting and sets the number of visible rows of items in each group.

## -parameters

### -param cVisibleRows [in]

Type: <b>UINT</b>

The number of rows to be visible.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If <i>cVisibleRows</i> is zero, subsetting is turned off.

