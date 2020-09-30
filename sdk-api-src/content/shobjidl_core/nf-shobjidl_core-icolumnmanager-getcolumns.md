---
UID: NF:shobjidl_core.IColumnManager.GetColumns
title: IColumnManager::GetColumns (shobjidl_core.h)
description: Gets an array of PROPERTYKEY structures that represent the columns that the view supports. Includes either all columns or only those currently visible.
helpviewer_keywords: ["GetColumns","GetColumns method [Windows Shell]","GetColumns method [Windows Shell]","IColumnManager interface","IColumnManager interface [Windows Shell]","GetColumns method","IColumnManager.GetColumns","IColumnManager::GetColumns","shell.IColumnManager_GetColumns","shell_IColumnManager_GetColumns","shobjidl_core/IColumnManager::GetColumns"]
old-location: shell\IColumnManager_GetColumns.htm
tech.root: shell
ms.assetid: 297a8e75-78a0-4bfb-83c0-0b58111dcf1c
ms.date: 12/05/2018
ms.keywords: GetColumns, GetColumns method [Windows Shell], GetColumns method [Windows Shell],IColumnManager interface, IColumnManager interface [Windows Shell],GetColumns method, IColumnManager.GetColumns, IColumnManager::GetColumns, shell.IColumnManager_GetColumns, shell_IColumnManager_GetColumns, shobjidl_core/IColumnManager::GetColumns
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IColumnManager::GetColumns
 - shobjidl_core/IColumnManager::GetColumns
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
 - IColumnManager.GetColumns
---

# IColumnManager::GetColumns


## -description

Gets an array of <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structures that represent the columns that the view supports. Includes either all columns or only those currently visible.

## -parameters

### -param dwFlags [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-cm_enum_flags">CM_ENUM_FLAGS</a></b>

A value from the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-cm_enum_flags">CM_ENUM_FLAGS</a> enumeration that specifies whether to show only visible columns or all columns regardless of visibility.

### -param rgkeyOrder [out]

Type: <b><a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a>*</b>

On success, contains a pointer to an array of <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structures that represent the columns.

### -param cColumns [in]

Type: <b>UINT</b>

The length of the <i>rgkeyOrder</i> array.

## -returns

Type: <b>HRESULT</b>

Returns one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Collection retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>failure</b></dt>
</dl>
</td>
<td width="60%">
All columns were not mapped to <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structures.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value in <i>cColumns</i> is inconsistent with the value in <i>dwFlags</i>.

</td>
</tr>
</table>