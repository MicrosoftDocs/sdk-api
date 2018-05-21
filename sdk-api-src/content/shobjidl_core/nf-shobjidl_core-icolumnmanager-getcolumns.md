---
UID: NF:shobjidl_core.IColumnManager.GetColumns
title: IColumnManager::GetColumns
author: windows-driver-content
description: Gets an array of PROPERTYKEY structures that represent the columns that the view supports. Includes either all columns or only those currently visible.
old-location: shell\IColumnManager_GetColumns.htm
old-project: shell
ms.assetid: 297a8e75-78a0-4bfb-83c0-0b58111dcf1c
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: GetColumns, GetColumns method [Windows Shell], GetColumns method [Windows Shell],IColumnManager interface, IColumnManager interface [Windows Shell],GetColumns method, IColumnManager.GetColumns, IColumnManager::GetColumns, shell.IColumnManager_GetColumns, shell_IColumnManager_GetColumns, shobjidl_core/IColumnManager::GetColumns
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	IColumnManager.GetColumns
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IColumnManager::GetColumns


## -description


Gets an array of <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> structures that represent the columns that the view supports. Includes either all columns or only those currently visible.


## -parameters




### -param dwFlags [in]

Type: <b><a href="https://msdn.microsoft.com/9706ae59-d172-4518-8090-375b1a0ff4fb">CM_ENUM_FLAGS</a></b>

A value from the <a href="https://msdn.microsoft.com/9706ae59-d172-4518-8090-375b1a0ff4fb">CM_ENUM_FLAGS</a> enumeration that specifies whether to show only visible columns or all columns regardless of visibility.


### -param rgkeyOrder [out]

Type: <b><a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a>*</b>

On success, contains a pointer to an array of <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> structures that represent the columns.


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
All columns were not mapped to <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> structures.

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
 



