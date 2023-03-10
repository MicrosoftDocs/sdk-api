---
UID: NF:shobjidl_core.IFolderView2.GetGroupSubsetCount
title: IFolderView2::GetGroupSubsetCount (shobjidl_core.h)
description: Gets the count of visible rows displayed for a group's subset.
helpviewer_keywords: ["GetGroupSubsetCount","GetGroupSubsetCount method [Windows Shell]","GetGroupSubsetCount method [Windows Shell]","IFolderView2 interface","IFolderView2 interface [Windows Shell]","GetGroupSubsetCount method","IFolderView2.GetGroupSubsetCount","IFolderView2::GetGroupSubsetCount","_shell_IFolderView2_GetGroupSubsetCount","shell.IFolderView2_GetGroupSubsetCount","shobjidl_core/IFolderView2::GetGroupSubsetCount"]
old-location: shell\IFolderView2_GetGroupSubsetCount.htm
tech.root: shell
ms.assetid: f377b9ec-6421-454f-b2d0-f3d1b537e2c3
ms.date: 12/05/2018
ms.keywords: GetGroupSubsetCount, GetGroupSubsetCount method [Windows Shell], GetGroupSubsetCount method [Windows Shell],IFolderView2 interface, IFolderView2 interface [Windows Shell],GetGroupSubsetCount method, IFolderView2.GetGroupSubsetCount, IFolderView2::GetGroupSubsetCount, _shell_IFolderView2_GetGroupSubsetCount, shell.IFolderView2_GetGroupSubsetCount, shobjidl_core/IFolderView2::GetGroupSubsetCount
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
 - IFolderView2::GetGroupSubsetCount
 - shobjidl_core/IFolderView2::GetGroupSubsetCount
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
 - IFolderView2.GetGroupSubsetCount
---

# IFolderView2::GetGroupSubsetCount


## -description

Gets the count of visible rows displayed for a group's subset.

## -parameters

### -param pcVisibleRows [out]

Type: <b>UINT*</b>

The number of rows currently visible.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If group subsetting is disabled the number of rows is zero.

