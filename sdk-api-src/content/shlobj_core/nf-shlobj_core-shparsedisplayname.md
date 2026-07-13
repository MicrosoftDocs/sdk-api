---
UID: NF:shlobj_core.SHParseDisplayName
title: SHParseDisplayName function (shlobj_core.h)
description: Translates a Shell namespace object's display name into an item identifier list and returns the attributes of the object. This function is the preferred method to convert a string to a pointer to an item identifier list (PIDL).
helpviewer_keywords: ["SHParseDisplayName","SHParseDisplayName function [Windows Shell]","_shell_SHParseDisplayName","shell.SHParseDisplayName","shlobj_core/SHParseDisplayName"]
old-location: shell\SHParseDisplayName.htm
tech.root: shell
ms.assetid: 7bdfeed5-dcd0-40f6-a9d0-08ce816ee055
ms.date: 12/05/2018
ms.keywords: SHParseDisplayName, SHParseDisplayName function [Windows Shell], _shell_SHParseDisplayName, shell.SHParseDisplayName, shlobj_core/SHParseDisplayName
req.header: shlobj_core.h
req.include-header: Shlobj.h
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHParseDisplayName
 - shlobj_core/SHParseDisplayName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shell32-l1-2-3.dll
 - api-ms-win-shell-namespace-l1-1-1.dll
 - Shell32.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
 - windows.storage.dll
 - API-MS-Win-Shell-Namespace-L1-1-0.dll
api_name:
 - SHParseDisplayName
---

# SHParseDisplayName function


## -description

Translates a Shell namespace object's display name into an item identifier list and returns the attributes of the object. This function is the preferred method to convert a string to a pointer to an item identifier list (PIDL).

## -parameters

### -param pszName [in]

Type: <b>LPCWSTR</b>

A pointer to a zero-terminated wide string that contains the display name to parse.

### -param pbc [in, optional]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>*</b>

A bind context that controls the parsing operation. This parameter is normally set to <b>NULL</b>.

### -param ppidl [out]

Type: <b>PIDLIST_ABSOLUTE*</b>

The address of a pointer to a variable of type <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> that receives the item identifier list for the object. If an error occurs, then this parameter is set to <b>NULL</b>.

### -param sfgaoIn [in]

Type: <b>SFGAOF</b>

A <b>ULONG</b> value that specifies the attributes to query. To query for one or more attributes, initialize this parameter with the flags that represent the attributes of interest. For a list of available SFGAO flags, see <a href="/windows/win32/shell/sfgao">SFGAO</a>.

### -param psfgaoOut [out, optional]

Type: <b>SFGAOF*</b>

A pointer to a <b>ULONG</b>. On return, those attributes that are true for the object and were requested in <i>sfgaoIn</i> are set. An object's attribute flags can be zero or a combination of SFGAO flags. For a list of available SFGAO flags, see <a href="/windows/win32/shell/sfgao">SFGAO</a>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You should call this function from a background thread. Failure to do so could cause the UI to stop responding.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof">IShellFolder::GetAttributesOf</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname">IShellFolder::ParseDisplayName</a>



<a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a>



<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista">SHGetPathFromIDList</a>
