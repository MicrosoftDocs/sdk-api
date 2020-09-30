---
UID: NF:shobjidl_core.IColumnManager.SetColumns
title: IColumnManager::SetColumns (shobjidl_core.h)
description: Sets the collection of columns for the view to display.
helpviewer_keywords: ["IColumnManager interface [Windows Shell]","SetColumns method","IColumnManager.SetColumns","IColumnManager::SetColumns","SetColumns","SetColumns method [Windows Shell]","SetColumns method [Windows Shell]","IColumnManager interface","shell.IColumnManager_SetColumns","shell_IColumnManager_SetColumns","shobjidl_core/IColumnManager::SetColumns"]
old-location: shell\IColumnManager_SetColumns.htm
tech.root: shell
ms.assetid: 1541809d-0826-46c4-aa10-cb4cbd6f8437
ms.date: 12/05/2018
ms.keywords: IColumnManager interface [Windows Shell],SetColumns method, IColumnManager.SetColumns, IColumnManager::SetColumns, SetColumns, SetColumns method [Windows Shell], SetColumns method [Windows Shell],IColumnManager interface, shell.IColumnManager_SetColumns, shell_IColumnManager_SetColumns, shobjidl_core/IColumnManager::SetColumns
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
 - IColumnManager::SetColumns
 - shobjidl_core/IColumnManager::SetColumns
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
 - IColumnManager.SetColumns
---

# IColumnManager::SetColumns


## -description

Sets the collection of columns for the view to display.

## -parameters

### -param rgkeyOrder [in]

Type: <b>const <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a>*</b>

A pointer to an array of <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structures that specify the columns to display.

### -param cVisible [in]

Type: <b>UINT</b>

The size of the <i>rgkeyOrder</i> array.

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
Collection set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>failure</b></dt>
</dl>
</td>
<td width="60%">
Collection not set.

</td>
</tr>
</table>

## -remarks

<div class="alert"><b>Note</b>  <b>IColumnManager::SetColumns</b> clears the state of all columns, so <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icolumnmanager-setcolumninfo">IColumnManager::SetColumnInfo</a> must be called afterward to set the state of individual columns.</div>
<div> </div>