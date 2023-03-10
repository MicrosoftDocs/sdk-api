---
UID: NF:shlobj.IColumnProvider.GetColumnInfo
title: IColumnProvider::GetColumnInfo (shlobj.h)
description: Requests information about a column.
helpviewer_keywords: ["GetColumnInfo","GetColumnInfo method [Windows Shell]","GetColumnInfo method [Windows Shell]","IColumnProvider interface","IColumnProvider interface [Windows Shell]","GetColumnInfo method","IColumnProvider.GetColumnInfo","IColumnProvider::GetColumnInfo","_win32_IColumnProvider_GetColumnInfo","shell.IColumnProvider_GetColumnInfo","shlobj/IColumnProvider::GetColumnInfo"]
old-location: shell\IColumnProvider_GetColumnInfo.htm
tech.root: shell
ms.assetid: 87196252-3835-4828-ad0a-0edcafb286b7
ms.date: 12/05/2018
ms.keywords: GetColumnInfo, GetColumnInfo method [Windows Shell], GetColumnInfo method [Windows Shell],IColumnProvider interface, IColumnProvider interface [Windows Shell],GetColumnInfo method, IColumnProvider.GetColumnInfo, IColumnProvider::GetColumnInfo, _win32_IColumnProvider_GetColumnInfo, shell.IColumnProvider_GetColumnInfo, shlobj/IColumnProvider::GetColumnInfo
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IColumnProvider::GetColumnInfo
 - shlobj/IColumnProvider::GetColumnInfo
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
 - IColumnProvider.GetColumnInfo
---

# IColumnProvider::GetColumnInfo


## -description

Requests information about a column.

## -parameters

### -param dwIndex

Type: <b>DWORD</b>

The column's zero-based index. It is an arbitrary value that is used to enumerate columns.

### -param psci [out]

Type: <b><a href="/windows/desktop/api/shlobj/ns-shlobj-shcolumninfo">SHCOLUMNINFO</a>*</b>

A pointer to an <a href="/windows/desktop/api/shlobj/ns-shlobj-shcolumninfo">SHCOLUMNINFO</a> structure to hold the column information.

## -returns

Type: <b>HRESULT</b>

Returns a COM error value to indicate that the request was unsuccessful or one of the following values.

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
Request successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Column index out of range.

</td>
</tr>
</table>

## -remarks

This method is called to assign an index to the column and to ask for details on what kind of information the column will contain.

## -see-also

<a href="/windows/desktop/api/shlobj/nn-shlobj-icolumnprovider">IColumnProvider</a>