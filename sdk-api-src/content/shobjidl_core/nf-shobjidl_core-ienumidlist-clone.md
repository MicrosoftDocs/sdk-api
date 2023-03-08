---
UID: NF:shobjidl_core.IEnumIDList.Clone
title: IEnumIDList::Clone (shobjidl_core.h)
description: Creates a new item enumeration object with the same contents and state as the current one. (IEnumIDList.Clone)
helpviewer_keywords: ["Clone","Clone method [Windows Shell]","Clone method [Windows Shell]","IEnumIDList interface","IEnumIDList interface [Windows Shell]","Clone method","IEnumIDList.Clone","IEnumIDList::Clone","_win32_IEnumIDList_Clone","shell.IEnumIDList_Clone","shobjidl_core/IEnumIDList::Clone"]
old-location: shell\IEnumIDList_Clone.htm
tech.root: shell
ms.assetid: f0118153-25ea-42d6-90bf-b85ffd99b74b
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Windows Shell], Clone method [Windows Shell],IEnumIDList interface, IEnumIDList interface [Windows Shell],Clone method, IEnumIDList.Clone, IEnumIDList::Clone, _win32_IEnumIDList_Clone, shell.IEnumIDList_Clone, shobjidl_core/IEnumIDList::Clone
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
 - IEnumIDList::Clone
 - shobjidl_core/IEnumIDList::Clone
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
 - IEnumIDList.Clone
---

# IEnumIDList::Clone


## -description

Creates a new item enumeration object with the same contents and state as the current one.

## -parameters

### -param ppenum

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist">IEnumIDList</a>**</b>

The address of a pointer to the new enumeration object. The calling application must eventually free the new object by calling its <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> member function.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error value otherwise.

## -remarks

This method makes it possible to record a particular point in the enumeration sequence and then return to that point at a later time.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist">IEnumIDList</a>
