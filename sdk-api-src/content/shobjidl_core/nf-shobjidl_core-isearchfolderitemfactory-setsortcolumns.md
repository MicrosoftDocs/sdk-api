---
UID: NF:shobjidl_core.ISearchFolderItemFactory.SetSortColumns
title: ISearchFolderItemFactory::SetSortColumns (shobjidl_core.h)
description: Creates a list of sort column directions, as specified.
helpviewer_keywords: ["ISearchFolderItemFactory interface [Windows Shell]","SetSortColumns method","ISearchFolderItemFactory.SetSortColumns","ISearchFolderItemFactory::SetSortColumns","SetSortColumns","SetSortColumns method [Windows Shell]","SetSortColumns method [Windows Shell]","ISearchFolderItemFactory interface","_shell_ISearchFolderItemFactory_SetSortColumns","shell.ISearchFolderItemFactory_SetSortColumns","shobjidl_core/ISearchFolderItemFactory::SetSortColumns"]
old-location: shell\ISearchFolderItemFactory_SetSortColumns.htm
tech.root: shell
ms.assetid: c91667fa-a48b-409a-ba96-35581fdd07dd
ms.date: 12/05/2018
ms.keywords: ISearchFolderItemFactory interface [Windows Shell],SetSortColumns method, ISearchFolderItemFactory.SetSortColumns, ISearchFolderItemFactory::SetSortColumns, SetSortColumns, SetSortColumns method [Windows Shell], SetSortColumns method [Windows Shell],ISearchFolderItemFactory interface, _shell_ISearchFolderItemFactory_SetSortColumns, shell.ISearchFolderItemFactory_SetSortColumns, shobjidl_core/ISearchFolderItemFactory::SetSortColumns
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
 - ISearchFolderItemFactory::SetSortColumns
 - shobjidl_core/ISearchFolderItemFactory::SetSortColumns
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
 - ISearchFolderItemFactory.SetSortColumns
---

# ISearchFolderItemFactory::SetSortColumns


## -description

Creates a list of sort column directions, as specified.

## -parameters

### -param cSortColumns [in]

Type: <b>UINT</b>

The number of sort columns.

### -param rgSortColumns [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-sortcolumn">SORTCOLUMN</a>*</b>

A pointer to an array of <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-sortcolumn">SORTCOLUMN</a> structures containing sort direction.  The default is <b>PKEY_ItemNameDisplay</b>.

## -returns

Type: <b>HRESULT</b>

Returns a success value if successful, or an error value otherwise.