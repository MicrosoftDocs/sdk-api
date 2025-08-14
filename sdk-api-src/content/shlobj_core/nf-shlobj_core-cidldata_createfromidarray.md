---
UID: NF:shlobj_core.CIDLData_CreateFromIDArray
title: CIDLData_CreateFromIDArray function (shlobj_core.h)
description: CIDLData_CreateFromIDArray may be altered or unavailable.
helpviewer_keywords: ["CIDLData_CreateFromIDArray","CIDLData_CreateFromIDArray function [Windows Shell]","_shell_CIDLData_CreateFromIDArray","shell.CIDLData_CreateFromIDArray","shlobj_core/CIDLData_CreateFromIDArray"]
old-location: shell\CIDLData_CreateFromIDArray.htm
tech.root: shell
ms.assetid: 4949c701-a375-450a-89a3-3fd146557d11
ms.date: 12/05/2018
ms.keywords: CIDLData_CreateFromIDArray, CIDLData_CreateFromIDArray function [Windows Shell], _shell_CIDLData_CreateFromIDArray, shell.CIDLData_CreateFromIDArray, shlobj_core/CIDLData_CreateFromIDArray
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CIDLData_CreateFromIDArray
 - shlobj_core/CIDLData_CreateFromIDArray
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shell32-l1-5-0.dll
 - ext-ms-win-shell-shell32-l1-4-0.dll
 - ext-ms-win-shell-shell32-l1-3-0.dll
 - ext-ms-win-shell-shell32-l1-2-3.dll
 - Shell32.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - CIDLData_CreateFromIDArray
req.apiset: ext-ms-win-shell-shell32-l1-2-1 (introduced in Windows 10, version 10.0.10240)
---

# CIDLData_CreateFromIDArray function


## -description

<p class="CCE_Message">[<b>CIDLData_CreateFromIDArray</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Creates a data object with the default vtable pointer.

## -parameters

### -param pidlFolder [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

A fully qualified IDLIST for the root of the items specified in <i>apidl</i>.

### -param cidl [in]

Type: <b>UINT</b>

The number of entries in the <i>apidl</i> array.

### -param apidl [in]

Type: <b>PCUIDLIST_RELATIVE_ARRAY</b>

The array of item IDs relative to <i>pidlFolder</i>. Typically, <i>apidl</i> is an array of child IDs and <i>pidlFolder</i> is a full PIDL for those items. However, <i>pidlFolder</i> can be a null PIDL (desktop IDLISTs). In that case, <i>apidl</i> can contain fully qualified ID lists.

### -param ppdtobj [out]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>**</b>

The address to a pointer to the object that implements <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The data object created by this function offers the Shell clipboard format identifier <a href="/windows/desktop/shell/clipboard">CFSTR_SHELLIDLIST</a>. This data object also supports <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-setdata">IDataObject::SetData</a> calls to pick up other clipboard formats.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedataobject">SHCreateDataObject</a>
