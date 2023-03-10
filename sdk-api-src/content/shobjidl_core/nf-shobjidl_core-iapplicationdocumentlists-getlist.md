---
UID: NF:shobjidl_core.IApplicationDocumentLists.GetList
title: IApplicationDocumentLists::GetList (shobjidl_core.h)
description: Retrieves an object that represents the collection of destinations listed in the Recent or Frequent category in a Jump List.
helpviewer_keywords: ["ADLT_FREQUENT","ADLT_RECENT","GetList","GetList method [Windows Shell]","GetList method [Windows Shell]","IApplicationDocumentLists interface","IApplicationDocumentLists interface [Windows Shell]","GetList method","IApplicationDocumentLists.GetList","IApplicationDocumentLists::GetList","_shell_IApplicationDocumentLists_GetList","shell.IApplicationDocumentLists_GetList","shobjidl_core/IApplicationDocumentLists::GetList"]
old-location: shell\IApplicationDocumentLists_GetList.htm
tech.root: shell
ms.assetid: d86bf039-81d9-4d43-9671-b107d7e925ab
ms.date: 12/05/2018
ms.keywords: ADLT_FREQUENT, ADLT_RECENT, GetList, GetList method [Windows Shell], GetList method [Windows Shell],IApplicationDocumentLists interface, IApplicationDocumentLists interface [Windows Shell],GetList method, IApplicationDocumentLists.GetList, IApplicationDocumentLists::GetList, _shell_IApplicationDocumentLists_GetList, shell.IApplicationDocumentLists_GetList, shobjidl_core/IApplicationDocumentLists::GetList
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.1 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IApplicationDocumentLists::GetList
 - shobjidl_core/IApplicationDocumentLists::GetList
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
 - IApplicationDocumentLists.GetList
---

# IApplicationDocumentLists::GetList


## -description

Retrieves an object that represents the collection of destinations listed in the <b>Recent</b> or <b>Frequent</b> category in a Jump List.

## -parameters

### -param listtype [in]

Type: <b>APPDOCLISTTYPE</b>

One of the following values that specifies from which category the list of destinations should be retrieved.



#### ADLT_RECENT (0x0)

0x0. The <b>Recent</b> category, which lists those items most recently accessed.



#### ADLT_FREQUENT (0x1)

0x1. The <b>Frequent</b> category, which lists the items that have been accessed the greatest number of times.

### -param cItemsDesired [in]

Type: <b>UINT</b>

The number of items to retrieve from the list specified in <i>listtype</i>. Set this parameter to 0 to retrieve the full list.

### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to retrieve through <i>ppv</i>, typically IID_IObjectArray or IID_IEnumObjects.

### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>. This is typically an <a href="/windows/desktop/api/objectarray/nn-objectarray-iobjectarray">IObjectArray</a> or <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumobjects">IEnumObjects</a> which represents a collection of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> or <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka">IShellLink</a> objects (or a mix of the two) that represent the retrieved items from the list.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

An item can appear in both the <b>Recent</b> and <b>Frequent</b> lists.

If a user pins an item in the <b>Recent</b> or <b>Frequent</b> categories, the item is no longer shown in its original category to avoid duplication in the Jump List. However, the item will still be returned by this method.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists">IApplicationDocumentLists</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-setappid">IApplicationDocumentLists::SetAppID</a>



<a href="/windows/desktop/shell/taskbar-extensions">Taskbar Extensions</a>