---
UID: NF:shobjidl_core.IColumnManager.GetColumnInfo
title: IColumnManager::GetColumnInfo (shobjidl_core.h)
description: Gets information about each column:\_width, visibility, display name, and state.
helpviewer_keywords: ["GetColumnInfo","GetColumnInfo method [Windows Shell]","GetColumnInfo method [Windows Shell]","IColumnManager interface","IColumnManager interface [Windows Shell]","GetColumnInfo method","IColumnManager.GetColumnInfo","IColumnManager::GetColumnInfo","shell.IColumnManager_GetColumnInfo","shell_IColumnManager_GetColumnInfo","shobjidl_core/IColumnManager::GetColumnInfo"]
old-location: shell\IColumnManager_GetColumnInfo.htm
tech.root: shell
ms.assetid: 22b3e5a6-a0a1-46e4-91b8-7bfe3944fffb
ms.date: 12/05/2018
ms.keywords: GetColumnInfo, GetColumnInfo method [Windows Shell], GetColumnInfo method [Windows Shell],IColumnManager interface, IColumnManager interface [Windows Shell],GetColumnInfo method, IColumnManager.GetColumnInfo, IColumnManager::GetColumnInfo, shell.IColumnManager_GetColumnInfo, shell_IColumnManager_GetColumnInfo, shobjidl_core/IColumnManager::GetColumnInfo
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
 - IColumnManager::GetColumnInfo
 - shobjidl_core/IColumnManager::GetColumnInfo
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
 - IColumnManager.GetColumnInfo
---

# IColumnManager::GetColumnInfo


## -description

Gets information about each column: width, visibility, display name, and state.

## -parameters

### -param propkey [in]

Type: <b>REFPROPERTYKEY</b>

A reference to a <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure.

### -param pcmci [in, out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cm_columninfo">CM_COLUMNINFO</a>*</b>

A pointer to a <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cm_columninfo">CM_COLUMNINFO</a> structure. On entry, set this structure's <b>dwMask</b> member to specify the information to retrieve. Also set its <b>cbSize</b> member. When this method returns successfully, the structure contains the requested information.

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
Column information obtained.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>failure</b></dt>
</dl>
</td>
<td width="60%">
Column information not obtained.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Indicates that cbSize member of <i>pcmci</i> does not equal the size of CM_COLUMNINFO.

</td>
</tr>
</table>