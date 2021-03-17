---
UID: NF:shobjidl_core.IShellFolder2.GetDefaultColumn
title: IShellFolder2::GetDefaultColumn (shobjidl_core.h)
description: Gets the default sorting and display columns.
helpviewer_keywords: ["GetDefaultColumn","GetDefaultColumn method [Windows Shell]","GetDefaultColumn method [Windows Shell]","IShellFolder2 interface","IShellFolder2 interface [Windows Shell]","GetDefaultColumn method","IShellFolder2.GetDefaultColumn","IShellFolder2::GetDefaultColumn","_win32_IShellFolder2_GetDefaultColumn","shell.IShellFolder2_GetDefaultColumn","shobjidl_core/IShellFolder2::GetDefaultColumn"]
old-location: shell\IShellFolder2_GetDefaultColumn.htm
tech.root: shell
ms.assetid: 5d1a1273-be67-4bb3-b549-8adacea0cb5f
ms.date: 12/05/2018
ms.keywords: GetDefaultColumn, GetDefaultColumn method [Windows Shell], GetDefaultColumn method [Windows Shell],IShellFolder2 interface, IShellFolder2 interface [Windows Shell],GetDefaultColumn method, IShellFolder2.GetDefaultColumn, IShellFolder2::GetDefaultColumn, _win32_IShellFolder2_GetDefaultColumn, shell.IShellFolder2_GetDefaultColumn, shobjidl_core/IShellFolder2::GetDefaultColumn
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellFolder2::GetDefaultColumn
 - shobjidl_core/IShellFolder2::GetDefaultColumn
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
 - IShellFolder2.GetDefaultColumn
---

# IShellFolder2::GetDefaultColumn


## -description

Gets the default sorting and display columns.

## -parameters

### -param dwRes [in]

Type: <b>DWORD</b>

Reserved. Set to zero.

### -param pSort [out]

Type: <b>ULONG*</b>

A pointer to a value that receives the index of the default sorted column.

### -param pDisplay [out]

Type: <b>ULONG*</b>

A pointer to a value that receives the index of the default display column.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM error value otherwise.

## -remarks

<h3><a id="Notes_to_Users"></a><a id="notes_to_users"></a><a id="NOTES_TO_USERS"></a>Notes to Users</h3>
Both column indexes returned by this method are intended for use by an application that is presenting a folder view of this folder.

The column specified by 
				<i>pSort</i> is the one that should be used for sorting the items in the folder. To determine the sorting order of any pair of items, pass their PIDLs to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids">CompareIDs</a>. Specify the column by setting the 
				<i>lParam</i> parameter of <b>CompareIDs</b> to the value pointed to by 
				<i>pSort</i>.

If a view will display only one string to represent an item, it should be taken from the column specified by 
				<i>pDisplay</i>. Pass the column index and the item's PIDL to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsof">IShellFolder2::GetDetailsOf</a> to retrieve the string.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
This method is part of a namespace extension's folder object implementation. It is typically called by a folder view object to ask the folder object which column in Microsoft Windows Explorer Details view should be used to sort the items in the folder. For example, a folder object that represents a transaction log might set 
				<i>pSort</i> to the column that displays the transaction time. The items will then be sorted by the time the transaction took place, rather than by name.

Some clients might call this method to request the index of the column with the names that should be displayed in tree view. Set 
				<i>pDisplay</i> to the appropriate column index. The client will then obtain the display names by calling <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsof">IShellFolder2::GetDetailsOf</a>.