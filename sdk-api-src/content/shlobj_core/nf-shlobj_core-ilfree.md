---
UID: NF:shlobj_core.ILFree
title: ILFree function (shlobj_core.h)
description: Frees an ITEMIDLIST structure allocated by the Shell.
helpviewer_keywords: ["HashTable_CoTaskMemFreeCB","ILFree","ILFree function [Windows Shell]","_win32_ILFree","shell.ILFree","shlobj_core/HashTable_CoTaskMemFreeCB","shlobj_core/ILFree"]
old-location: shell\ILFree.htm
tech.root: shell
ms.assetid: 3457f36e-fdfd-44a4-90ca-a86f00bc9f36
ms.date: 12/05/2018
ms.keywords: HashTable_CoTaskMemFreeCB, ILFree, ILFree function [Windows Shell], _win32_ILFree, shell.ILFree, shlobj_core/HashTable_CoTaskMemFreeCB, shlobj_core/ILFree
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ILFree
 - shlobj_core/ILFree
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
 - Windows.Storage.dll
 - API-MS-Win-Shell-Namespace-L1-1-0.dll
api_name:
 - ILFree
 - HashTable_CoTaskMemFreeCB
---

# ILFree function


## -description

Frees an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure allocated by the Shell.

## -parameters

### -param pidl [in]

Type: <b>PIDLIST_RELATIVE</b>

A pointer to the <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure to be freed. This parameter can be <b>NULL</b>.

## -remarks

<b>ILFree</b> is often used with <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structures allocated by one of the other IL functions, but it can be used to free any such structure returned by the Shell—for example, the <b>ITEMIDLIST</b> structure returned by <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera">SHBrowseForFolder</a> or used in a call to <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation">SHGetFolderLocation</a>.

<div class="alert"><b>Note</b>  When using Windows 2000 or later, use <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> rather than <b>ILFree</b>. <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structures are always allocated with the Component Object Model (COM) task allocator on those platforms.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilappendid">ILAppendID</a>



<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilclone">ILClone</a>



<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilclonefirst">ILCloneFirst</a>



<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilcombine">ILCombine</a>