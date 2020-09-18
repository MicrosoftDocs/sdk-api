---
UID: NF:shobjidl_core.ISearchFolderItemFactory.SetGroupColumn
title: ISearchFolderItemFactory::SetGroupColumn (shobjidl_core.h)
description: Sets a group column, as specified. If no group column is specified, no grouping occurs.
helpviewer_keywords: ["ISearchFolderItemFactory interface [Windows Shell]","SetGroupColumn method","ISearchFolderItemFactory.SetGroupColumn","ISearchFolderItemFactory::SetGroupColumn","SetGroupColumn","SetGroupColumn method [Windows Shell]","SetGroupColumn method [Windows Shell]","ISearchFolderItemFactory interface","_shell_ISearchFolderItemFactory_SetGroupColumn","shell.ISearchFolderItemFactory_SetGroupColumn","shobjidl_core/ISearchFolderItemFactory::SetGroupColumn"]
old-location: shell\ISearchFolderItemFactory_SetGroupColumn.htm
tech.root: shell
ms.assetid: 52967ebe-3a8c-4696-aa5d-251a4cf58469
ms.date: 12/05/2018
ms.keywords: ISearchFolderItemFactory interface [Windows Shell],SetGroupColumn method, ISearchFolderItemFactory.SetGroupColumn, ISearchFolderItemFactory::SetGroupColumn, SetGroupColumn, SetGroupColumn method [Windows Shell], SetGroupColumn method [Windows Shell],ISearchFolderItemFactory interface, _shell_ISearchFolderItemFactory_SetGroupColumn, shell.ISearchFolderItemFactory_SetGroupColumn, shobjidl_core/ISearchFolderItemFactory::SetGroupColumn
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
 - ISearchFolderItemFactory::SetGroupColumn
 - shobjidl_core/ISearchFolderItemFactory::SetGroupColumn
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
 - ISearchFolderItemFactory.SetGroupColumn
---

# ISearchFolderItemFactory::SetGroupColumn


## -description

Sets a group column, as specified. If no group column is specified, no grouping occurs.

## -parameters

### -param keyGroup [in]

Type: <b>REFPROPERTYKEY</b>

A reference to a group column <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a>.

## -returns

Type: <b>HRESULT</b>

Returns a success value if successful, or an error value otherwise.