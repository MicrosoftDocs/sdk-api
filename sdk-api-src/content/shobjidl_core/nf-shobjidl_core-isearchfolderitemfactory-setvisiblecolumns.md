---
UID: NF:shobjidl_core.ISearchFolderItemFactory.SetVisibleColumns
title: ISearchFolderItemFactory::SetVisibleColumns (shobjidl_core.h)
description: Creates a new column list whose columns are all visible, given an array of PROPERTYKEY structures. The default is based on FolderTypeID.
helpviewer_keywords: ["ISearchFolderItemFactory interface [Windows Shell]","SetVisibleColumns method","ISearchFolderItemFactory.SetVisibleColumns","ISearchFolderItemFactory::SetVisibleColumns","SetVisibleColumns","SetVisibleColumns method [Windows Shell]","SetVisibleColumns method [Windows Shell]","ISearchFolderItemFactory interface","_shell_ISearchFolderItemFactory_SetVisibleColumns","shell.ISearchFolderItemFactory_SetVisibleColumns","shobjidl_core/ISearchFolderItemFactory::SetVisibleColumns"]
old-location: shell\ISearchFolderItemFactory_SetVisibleColumns.htm
tech.root: shell
ms.assetid: be18218e-a117-4256-936e-3a5eb36c3654
ms.date: 12/05/2018
ms.keywords: ISearchFolderItemFactory interface [Windows Shell],SetVisibleColumns method, ISearchFolderItemFactory.SetVisibleColumns, ISearchFolderItemFactory::SetVisibleColumns, SetVisibleColumns, SetVisibleColumns method [Windows Shell], SetVisibleColumns method [Windows Shell],ISearchFolderItemFactory interface, _shell_ISearchFolderItemFactory_SetVisibleColumns, shell.ISearchFolderItemFactory_SetVisibleColumns, shobjidl_core/ISearchFolderItemFactory::SetVisibleColumns
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
 - ISearchFolderItemFactory::SetVisibleColumns
 - shobjidl_core/ISearchFolderItemFactory::SetVisibleColumns
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
 - ISearchFolderItemFactory.SetVisibleColumns
---

# ISearchFolderItemFactory::SetVisibleColumns


## -description

Creates a new column list whose columns are all visible, given an array of <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structures. The default is based on <b>FolderTypeID</b>.

## -parameters

### -param cVisibleColumns [in]

Type: <b>UINT</b>

The number of array elements.

### -param rgKey [in]

Type: <b>const <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a>*</b>

A pointer to an array of <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structures.

## -returns

Type: <b>HRESULT</b>

Returns a success value if successful, or an error value otherwise.