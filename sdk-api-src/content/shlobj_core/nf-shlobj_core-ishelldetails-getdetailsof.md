---
UID: NF:shlobj_core.IShellDetails.GetDetailsOf
title: IShellDetails::GetDetailsOf (shlobj_core.h)
description: Gets detailed information on an item in a Shell folder.
helpviewer_keywords: ["GetDetailsOf","GetDetailsOf method [Windows Shell]","GetDetailsOf method [Windows Shell]","IShellDetails interface","IShellDetails interface [Windows Shell]","GetDetailsOf method","IShellDetails.GetDetailsOf","IShellDetails::GetDetailsOf","_win32_IShellDetails_GetDetailsOf","shell.IShellDetails_GetDetailsOf","shlobj_core/IShellDetails::GetDetailsOf"]
old-location: shell\IShellDetails_GetDetailsOf.htm
tech.root: shell
ms.assetid: 5442dc80-9ecf-4e47-a84d-6da4327696ef
ms.date: 12/05/2018
ms.keywords: GetDetailsOf, GetDetailsOf method [Windows Shell], GetDetailsOf method [Windows Shell],IShellDetails interface, IShellDetails interface [Windows Shell],GetDetailsOf method, IShellDetails.GetDetailsOf, IShellDetails::GetDetailsOf, _win32_IShellDetails_GetDetailsOf, shell.IShellDetails_GetDetailsOf, shlobj_core/IShellDetails::GetDetailsOf
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - IShellDetails::GetDetailsOf
 - shlobj_core/IShellDetails::GetDetailsOf
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
 - IShellDetails.GetDetailsOf
---

# IShellDetails::GetDetailsOf


## -description

Gets detailed information on an item in a Shell folder.

## -parameters

### -param pidl [in, optional]

Type: <b>PCUITEMID_CHILD</b>

The PIDL of the item that you are requesting information for. If this parameter is set to <b>NULL</b>, the title of the information field specified by <i>iColumn</i> will be returned in the <a href="/windows/desktop/api/shtypes/ns-shtypes-shelldetails">SHELLDETAILS</a> structure pointed to by <i>pDetails</i>.

### -param iColumn

Type: <b>UINT</b>

The zero-based index of the desired information field. It is identical to column number of the information as it is displayed in a Windows Explorer Details view.

### -param pDetails [out]

Type: <b>SHELLDETAILS*</b>

A pointer to a <a href="/windows/desktop/api/shtypes/ns-shtypes-shelldetails">SHELLDETAILS</a> structure with the detail information.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful. Returns E_FAIL if <i>iColumn</i> exceeds the number of columns supported by the folder. Otherwise, returns a standard COM error code.

## -remarks

This method has been superseded by the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2">IShellFolder2</a> methods for Shell <a href="/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)">version 5.0</a> and later.

The <b>IShellDetails::GetDetailsOf</b> method provides access to the information that is displayed in the Windows Explorer Details view of a Shell folder. The column numbers, column titles, and item information that you see in the Details view are identical to those returned by <b>IShellDetails::GetDetailsOf</b>.

The available information fields and their column numbers vary depending on the particular folder. To enumerate the available fields call <b>IShellDetails::GetDetailsOf</b> with <i>pidl</i> set to <b>NULL</b> for increasing values of <i>iColumn</i>. This approach provides you with the title associated with each column index. When <i>iColumn</i> exceeds the number of columns supported by the folder, <b>IShellDetails::GetDetailsOf</b> will return E_FAIL. Bear in mind that these titles are localizable, and may not be the same for all locales.

File system folders have a large standard set of information fields. The first four fields are standard for all file system folders.
                
                

<table class="clsStd">
<tr>
<th>Column Index</th>
<th>Column Title</th>
</tr>
<tr>
<td>0</td>
<td>Name</td>
</tr>
<tr>
<td>1</td>
<td>Size</td>
</tr>
<tr>
<td>2</td>
<td>Type</td>
</tr>
<tr>
<td>3</td>
<td>Date Modified</td>
</tr>
</table>
 

File system folders may support a number of additional fields. However, they are not required to do so and the column indexes assigned to these fields may vary.

Each virtual folder has its own unique set of information fields. Typically, the item's display name is in column zero, but the order and content of the available fields depend on the implementation of the particular folder object.

<h3><a id="Note_to_Implementers"></a><a id="note_to_implementers"></a><a id="NOTE_TO_IMPLEMENTERS"></a>Note to Implementers</h3>
Folder objects should implement <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2">IShellFolder2</a> instead of this interface.