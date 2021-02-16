---
UID: NF:shobjidl.IEnumerableView.CreateEnumIDListFromContents
title: IEnumerableView::CreateEnumIDListFromContents (shobjidl.h)
description: Creates an enumerator of ID lists from the contents of the view.
helpviewer_keywords: ["CreateEnumIDListFromContents","CreateEnumIDListFromContents method [Windows Shell]","CreateEnumIDListFromContents method [Windows Shell]","IEnumerableView interface","IEnumerableView interface [Windows Shell]","CreateEnumIDListFromContents method","IEnumerableView.CreateEnumIDListFromContents","IEnumerableView::CreateEnumIDListFromContents","_shell_IEnumerableView_CreateEnumIDListFromContents","shell.IEnumerableView_CreateEnumIDListFromContents","shobjidl/IEnumerableView::CreateEnumIDListFromContents"]
old-location: shell\IEnumerableView_CreateEnumIDListFromContents.htm
tech.root: shell
ms.assetid: 413d913d-e6f3-4e2d-bf1f-5d5ad6d4f650
ms.date: 12/05/2018
ms.keywords: CreateEnumIDListFromContents, CreateEnumIDListFromContents method [Windows Shell], CreateEnumIDListFromContents method [Windows Shell],IEnumerableView interface, IEnumerableView interface [Windows Shell],CreateEnumIDListFromContents method, IEnumerableView.CreateEnumIDListFromContents, IEnumerableView::CreateEnumIDListFromContents, _shell_IEnumerableView_CreateEnumIDListFromContents, shell.IEnumerableView_CreateEnumIDListFromContents, shobjidl/IEnumerableView::CreateEnumIDListFromContents
req.header: shobjidl.h
req.include-header: 
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
 - IEnumerableView::CreateEnumIDListFromContents
 - shobjidl/IEnumerableView::CreateEnumIDListFromContents
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IEnumerableView.CreateEnumIDListFromContents
---

# IEnumerableView::CreateEnumIDListFromContents


## -description

Creates an enumerator of ID lists from the contents of the view.

## -parameters

### -param pidlFolder [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

A PIDL that is relative to the Desktop.

### -param dwEnumFlags [in]

Type: <b>DWORD</b>

Specifies enumeration flags. See the <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf">SHCONTF</a> enumerated type.

### -param ppEnumIDList [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist">IEnumIDList</a>**</b>

When this method returns, contains an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist">IEnumIDList</a> interface pointer.

## -returns

Type: <b>HRESULT</b>

Returns a success value if successful, or an error value otherwise.