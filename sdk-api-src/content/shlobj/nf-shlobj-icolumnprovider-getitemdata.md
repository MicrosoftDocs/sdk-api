---
UID: NF:shlobj.IColumnProvider.GetItemData
title: IColumnProvider::GetItemData (shlobj.h)
description: Requests column data for a specified file.
helpviewer_keywords: ["GetItemData","GetItemData method [Windows Shell]","GetItemData method [Windows Shell]","IColumnProvider interface","IColumnProvider interface [Windows Shell]","GetItemData method","IColumnProvider.GetItemData","IColumnProvider::GetItemData","_win32_IColumnProvider_GetItemData","shell.IColumnProvider_GetItemData","shlobj/IColumnProvider::GetItemData"]
old-location: shell\IColumnProvider_GetItemData.htm
tech.root: shell
ms.assetid: 88e76f03-acc3-46b1-ad03-d2343f4f3dac
ms.date: 12/05/2018
ms.keywords: GetItemData, GetItemData method [Windows Shell], GetItemData method [Windows Shell],IColumnProvider interface, IColumnProvider interface [Windows Shell],GetItemData method, IColumnProvider.GetItemData, IColumnProvider::GetItemData, _win32_IColumnProvider_GetItemData, shell.IColumnProvider_GetItemData, shlobj/IColumnProvider::GetItemData
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
 - IColumnProvider::GetItemData
 - shlobj/IColumnProvider::GetItemData
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
 - IColumnProvider.GetItemData
---

# IColumnProvider::GetItemData


## -description

Requests column data for a specified file.

## -parameters

### -param pscid [in]

Type: <b>LPCSHCOLUMNID</b>

An <a href="/windows/desktop/shell/objects">SHCOLUMNID</a> structure that identifies the column.

### -param pscd [in]

Type: <b>LPCSHCOLUMNDATA</b>

An <a href="/windows/desktop/api/shlobj/ns-shlobj-shcolumndata">SHCOLUMNDATA</a> structure that specifies the file.

### -param pvarData [out]

Type: <b>VARIANT*</b>

A pointer to a <b>VARIANT</b> with the data for the file specified by <i>pscd</i> that belongs in the column specified by <i>pscid</i>. Set this value if the file is a member of the class supported by the column provider.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if file data is returned, S_FALSE if the file is not supported by the column provider and no data is returned, or a COM error value otherwise.

## -remarks

This method is called to retrieve the data for a file to be displayed in the specified column. It should be thread-safe.

This method is called for every file that Windows Explorer displays, even though many of them will not be supported by a particular column provider. To improve performance, first check the <b>pwszExt</b> member of the structure pointed to by <i>pscd</i> to see if it has a file name extension that is supported by the column provider. If not, avoid unnecessary processing by immediately returning S_FALSE.