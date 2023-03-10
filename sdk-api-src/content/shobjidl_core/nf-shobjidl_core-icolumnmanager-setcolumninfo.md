---
UID: NF:shobjidl_core.IColumnManager.SetColumnInfo
title: IColumnManager::SetColumnInfo (shobjidl_core.h)
description: Sets the state for a specified column.
helpviewer_keywords: ["IColumnManager interface [Windows Shell]","SetColumnInfo method","IColumnManager.SetColumnInfo","IColumnManager::SetColumnInfo","SetColumnInfo","SetColumnInfo method [Windows Shell]","SetColumnInfo method [Windows Shell]","IColumnManager interface","shell.IColumnManager_SetColumnInfo","shell_IColumnManager_SetColumnInfo","shobjidl_core/IColumnManager::SetColumnInfo"]
old-location: shell\IColumnManager_SetColumnInfo.htm
tech.root: shell
ms.assetid: 3a52d634-0ff0-4dbc-81cb-90cdffe4f6ae
ms.date: 12/05/2018
ms.keywords: IColumnManager interface [Windows Shell],SetColumnInfo method, IColumnManager.SetColumnInfo, IColumnManager::SetColumnInfo, SetColumnInfo, SetColumnInfo method [Windows Shell], SetColumnInfo method [Windows Shell],IColumnManager interface, shell.IColumnManager_SetColumnInfo, shell_IColumnManager_SetColumnInfo, shobjidl_core/IColumnManager::SetColumnInfo
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
 - IColumnManager::SetColumnInfo
 - shobjidl_core/IColumnManager::SetColumnInfo
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
 - IColumnManager.SetColumnInfo
---

# IColumnManager::SetColumnInfo


## -description

Sets the state for a specified column.

## -parameters

### -param propkey [in]

Type: <b>REFPROPERTYKEY</b>

A reference to a <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure that identifies the column.

### -param pcmci [in]

Type: <b>const <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cm_columninfo">CM_COLUMNINFO</a>*</b>

A pointer to a <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cm_columninfo">CM_COLUMNINFO</a> structure that contains the state to set for this column.

## -returns

Type: <b>HRESULT</b>

Returns one of the following values.

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
Column state set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>failure</b></dt>
</dl>
</td>
<td width="60%">
Column state not set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pcmci</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>