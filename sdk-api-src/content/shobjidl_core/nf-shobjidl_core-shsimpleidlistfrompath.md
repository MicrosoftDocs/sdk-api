---
UID: NF:shobjidl_core.SHSimpleIDListFromPath
title: SHSimpleIDListFromPath function (shobjidl_core.h)
description: Deprecated. Returns a pointer to an ITEMIDLIST structure when passed a path.
helpviewer_keywords: ["SHSimpleIDListFromPath","SHSimpleIDListFromPath function [Windows Shell]","_win32_SHSimpleIDListFromPath","shell.SHSimpleIDListFromPath","shobjidl_core/SHSimpleIDListFromPath"]
old-location: shell\SHSimpleIDListFromPath.htm
tech.root: shell
ms.assetid: 349974c2-4ab9-4eb2-897d-a5934893ed07
ms.date: 12/05/2018
ms.keywords: SHSimpleIDListFromPath, SHSimpleIDListFromPath function [Windows Shell], _win32_SHSimpleIDListFromPath, shell.SHSimpleIDListFromPath, shobjidl_core/SHSimpleIDListFromPath
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
req.dll: Shell32.dll (version 5.00 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHSimpleIDListFromPath
 - shobjidl_core/SHSimpleIDListFromPath
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
 - SHSimpleIDListFromPath
req.apiset: ext-ms-win-shell-shell32-l1-2-1 (introduced in Windows 10, version 10.0.10240)
---

# SHSimpleIDListFromPath function


## -description

Deprecated. Returns a pointer to an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure when passed a path.

## -parameters

### -param pszPath [in]

Type: <b>PCWSTR</b>

A pointer to a null-terminated string that contains the path to be converted to a PIDL.

## -returns

Type: <b>PIDLIST_ABSOLUTE</b>

Returns a pointer to an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure if successful, or <b>NULL</b> otherwise.

## -remarks

Prior to Windows 7, this function was declared in Shlobj.h. In Windows 7 and later versions, it is declared in Shobjidl.h.

<div class="alert"><b>Note</b>  This function is available through Windows 7 and Windows Server 2003. It is possible that it will not be present in future versions of Windows.</div>
<div> </div>
An alternative to this function is as follows:
                
                

<ol>
<li>Call <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder">SHGetDesktopFolder</a> to obtain <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> for the desktop folder.</li>
<li>Get the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>'s bind context (<a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>).</li>
<li>Call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname">IShellFolder::ParseDisplayName</a> with the <a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a> and the path.</li>
</ol>
