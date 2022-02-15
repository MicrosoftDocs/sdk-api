---
UID: NF:shobjidl_core.IFolderView2.SetSortColumns
title: IFolderView2::SetSortColumns (shobjidl_core.h)
description: Sets and sorts the view by the given sort columns.
helpviewer_keywords: ["IFolderView2 interface [Windows Shell]","SetSortColumns method","IFolderView2.SetSortColumns","IFolderView2::SetSortColumns","SetSortColumns","SetSortColumns method [Windows Shell]","SetSortColumns method [Windows Shell]","IFolderView2 interface","_shell_IFolderView2_SetSortColumns","shell.IFolderView2_SetSortColumns","shobjidl_core/IFolderView2::SetSortColumns"]
old-location: shell\IFolderView2_SetSortColumns.htm
tech.root: shell
ms.assetid: 54dfac6b-8355-4064-9f54-4172975b8028
ms.date: 12/05/2018
ms.keywords: IFolderView2 interface [Windows Shell],SetSortColumns method, IFolderView2.SetSortColumns, IFolderView2::SetSortColumns, SetSortColumns, SetSortColumns method [Windows Shell], SetSortColumns method [Windows Shell],IFolderView2 interface, _shell_IFolderView2_SetSortColumns, shell.IFolderView2_SetSortColumns, shobjidl_core/IFolderView2::SetSortColumns
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
 - IFolderView2::SetSortColumns
 - shobjidl_core/IFolderView2::SetSortColumns
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
 - IFolderView2.SetSortColumns
---

# IFolderView2::SetSortColumns


## -description

Sets and sorts the view by the given sort columns.

## -parameters

### -param rgSortColumns [in]

Type: <b>const <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-sortcolumn">SORTCOLUMN</a>*</b>

A pointer to a <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-sortcolumn">SORTCOLUMN</a> structure. The size of this structure is determined by <i>cColumns</i>.

### -param cColumns [in]

Type: <b>int</b>

The count of columns to sort by.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.