---
UID: NF:shobjidl_core.IShellFolder2.GetDetailsOf
title: IShellFolder2::GetDetailsOf (shobjidl_core.h)
description: Gets detailed information, identified by a column index, on an item in a Shell folder.
helpviewer_keywords: ["GetDetailsOf","GetDetailsOf method [Windows Shell]","GetDetailsOf method [Windows Shell]","IShellFolder2 interface","IShellFolder2 interface [Windows Shell]","GetDetailsOf method","IShellFolder2.GetDetailsOf","IShellFolder2::GetDetailsOf","_win32_IShellFolder2_GetDetailsOf","shell.IShellFolder2_GetDetailsOf","shobjidl_core/IShellFolder2::GetDetailsOf"]
old-location: shell\IShellFolder2_GetDetailsOf.htm
tech.root: shell
ms.assetid: bd9e8b6c-ed70-455e-8316-ac0868493802
ms.date: 12/05/2018
ms.keywords: GetDetailsOf, GetDetailsOf method [Windows Shell], GetDetailsOf method [Windows Shell],IShellFolder2 interface, IShellFolder2 interface [Windows Shell],GetDetailsOf method, IShellFolder2.GetDetailsOf, IShellFolder2::GetDetailsOf, _win32_IShellFolder2_GetDetailsOf, shell.IShellFolder2_GetDetailsOf, shobjidl_core/IShellFolder2::GetDetailsOf
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
 - IShellFolder2::GetDetailsOf
 - shobjidl_core/IShellFolder2::GetDetailsOf
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
 - IShellFolder2.GetDetailsOf
---

# IShellFolder2::GetDetailsOf


## -description

Gets detailed information, identified by a column index, on an item in a Shell folder.

## -parameters

### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

PIDL of the item for which you are requesting information. This method accepts only single-level PIDLs. The structure must contain exactly one <a href="/windows/desktop/api/shtypes/ns-shtypes-shitemid">SHITEMID</a> structure followed by a terminating zero. If this parameter is set to <b>NULL</b>, the title of the information field specified by <i>iColumn</i> is returned.

### -param iColumn [in]

Type: <b>UINT</b>

The zero-based index of the desired information field. It is identical to the column number of the information as it is displayed in a Windows Explorer Details view.

### -param psd [out]

Type: <b><a href="/windows/desktop/api/shtypes/ns-shtypes-shelldetails">SHELLDETAILS</a>*</b>

A pointer to a <a href="/windows/desktop/api/shtypes/ns-shtypes-shelldetails">SHELLDETAILS</a> structure that contains the information.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>IShellFolder2::GetDetailsOf</b> method is identical to <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ishelldetails-getdetailsof">GetDetailsOf</a>. For a more robust way to retrieve item information that does not require you to know the column index, use <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex">IShellFolder2::GetDetailsEx</a>.

The <b>IShellFolder2::GetDetailsOf</b> method provides access to the information that is displayed in the Windows Explorer Details view of a Shell folder. The column numbers, headings, and information that you see in the Details view are identical to those of <b>IShellFolder2::GetDetailsOf</b>. Note that the available information fields and their column numbers vary depending on the particular folder. You can enumerate the available fields by calling this method with <i>pidl</i> set to <b>NULL</b>, and examining the title associated with each column index. Bear in mind that these titles can be localized and might not be the same for all locales.

File system folders have a large, standard set of information fields. The first four fields are standard for all file system folders.

<table class="clsStd">
<tr>
<th>Column index</th>
<th>Column title</th>
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
 

File system folders can support a number of additional fields. However, they are not required to do so, and the column indexes assigned to these fields might vary.

Each virtual folder has its own unique set of information fields. Normally, the item's display name is in column zero, but the order and content of the remaining fields depend on the implementation of the particular folder object.