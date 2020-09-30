---
UID: NF:shobjidl_core.IEnumIDList.Skip
title: IEnumIDList::Skip (shobjidl_core.h)
description: Skips the specified number of elements in the enumeration sequence.
helpviewer_keywords: ["IEnumIDList interface [Windows Shell]","Skip method","IEnumIDList.Skip","IEnumIDList::Skip","Skip","Skip method [Windows Shell]","Skip method [Windows Shell]","IEnumIDList interface","_win32_IEnumIDList_Skip","shell.IEnumIDList_Skip","shobjidl_core/IEnumIDList::Skip"]
old-location: shell\IEnumIDList_Skip.htm
tech.root: shell
ms.assetid: ed9d5774-7b2f-4a25-88f9-70d72919ff60
ms.date: 12/05/2018
ms.keywords: IEnumIDList interface [Windows Shell],Skip method, IEnumIDList.Skip, IEnumIDList::Skip, Skip, Skip method [Windows Shell], Skip method [Windows Shell],IEnumIDList interface, _win32_IEnumIDList_Skip, shell.IEnumIDList_Skip, shobjidl_core/IEnumIDList::Skip
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumIDList::Skip
 - shobjidl_core/IEnumIDList::Skip
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IEnumIDList.Skip
---

# IEnumIDList::Skip


## -description

Skips the specified number of elements in the enumeration sequence.

## -parameters

### -param celt

Type: <b>ULONG</b>

The number of item identifiers to skip.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error value otherwise.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist">IEnumIDList</a>