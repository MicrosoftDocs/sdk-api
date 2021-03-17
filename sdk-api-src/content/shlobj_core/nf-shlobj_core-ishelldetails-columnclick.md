---
UID: NF:shlobj_core.IShellDetails.ColumnClick
title: IShellDetails::ColumnClick (shlobj_core.h)
description: Rearranges a column.
helpviewer_keywords: ["ColumnClick","ColumnClick method [Windows Shell]","ColumnClick method [Windows Shell]","IShellDetails interface","IShellDetails interface [Windows Shell]","ColumnClick method","IShellDetails.ColumnClick","IShellDetails::ColumnClick","_win32_IShellDetails_ColumnClick","shell.IShellDetails_ColumnClick","shlobj_core/IShellDetails::ColumnClick"]
old-location: shell\IShellDetails_ColumnClick.htm
tech.root: shell
ms.assetid: df37b2c7-16ea-4768-a1c2-6ccec4fecde9
ms.date: 12/05/2018
ms.keywords: ColumnClick, ColumnClick method [Windows Shell], ColumnClick method [Windows Shell],IShellDetails interface, IShellDetails interface [Windows Shell],ColumnClick method, IShellDetails.ColumnClick, IShellDetails::ColumnClick, _win32_IShellDetails_ColumnClick, shell.IShellDetails_ColumnClick, shlobj_core/IShellDetails::ColumnClick
req.header: shlobj_core.h
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
 - IShellDetails::ColumnClick
 - shlobj_core/IShellDetails::ColumnClick
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
 - IShellDetails.ColumnClick
---

# IShellDetails::ColumnClick


## -description

Rearranges a column.

## -parameters

### -param iColumn

Type: <b>UINT</b>

The index of the column to be rearranged.

## -returns

Type: <b>HRESULT</b>

Returns S_FALSE to tell the calling application to sort the selected column. Otherwise, returns S_OK if successful, a COM error code otherwise.

## -remarks

This method is called when a client of a folder object wants to sort the object's items based on the contents of one of the Details columns. Folder objects typically return S_FALSE.

<h3><a id="Note_to_Implementers"></a><a id="note_to_implementers"></a><a id="NOTE_TO_IMPLEMENTERS"></a>Note to Implementers</h3>
For Windows 2000 and later systems, folder objects should implement <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2">IShellFolder2</a> instead of this interface. However, if your application needs to function on earlier systems, it should also expose <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishelldetails">IShellDetails</a>.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishelldetails">IShellDetails</a>



<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ishelldetails-getdetailsof">IShellDetails::GetDetailsOf</a>