---
UID: NF:shlobj_core.SHCreateShellFolderView
title: SHCreateShellFolderView function (shlobj_core.h)
description: Creates a new instance of the default Shell folder view object (DefView).
helpviewer_keywords: ["SHCreateShellFolderView","SHCreateShellFolderView function [Windows Shell]","_win32_SHCreateShellFolderView","shell.SHCreateShellFolderView","shlobj_core/SHCreateShellFolderView"]
old-location: shell\SHCreateShellFolderView.htm
tech.root: shell
ms.assetid: f2948a6d-84a5-456b-b328-ba76dba46e9d
ms.date: 12/05/2018
ms.keywords: SHCreateShellFolderView, SHCreateShellFolderView function [Windows Shell], _win32_SHCreateShellFolderView, shell.SHCreateShellFolderView, shlobj_core/SHCreateShellFolderView
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
 - SHCreateShellFolderView
 - shlobj_core/SHCreateShellFolderView
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHCreateShellFolderView
req.apiset: ext-ms-win-shell-shell32-l1-2-2 (introduced in Windows 10, version 10.0.14393)
---

# SHCreateShellFolderView function


## -description

Creates a new instance of the default Shell folder view object (DefView).

## -parameters

### -param pcsfv [in]

Type: <b>const <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-sfv_create">SFV_CREATE</a>*</b>

Pointer to a <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-sfv_create">SFV_CREATE</a> structure that describes the particulars used in creating this instance of the Shell folder view object.

### -param ppsv [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>**</b>

When this function returns successfully, contains an interface pointer to the new <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> object. On failure, this value is <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>SHCreateShellFolderView</b> is recommended over <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex">SHCreateShellFolderViewEx</a> because of the greater flexibility of its elements to participate in various scenarios, provide new functionality to the view, and interact with other objects.

When dealing with several instances of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>, you might want to verify which is the default Shell folder view object. To do so, call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on the object using the IID_CDefView IID. This call succeeds only when made on the default Shell folder view object.

Data sources that use the default Shell folder view object must implement these interfaces:
                
                

<ul>
<li>
<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>
</li>
<li>
<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2">IShellFolder2</a>
</li>
<li>
<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder">IPersistFolder</a>
</li>
<li>
<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder2">IPersistFolder2</a>
</li>
</ul>
Optionally, they can also implement <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder3">IPersistFolder3</a>.

## -see-also

<a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-sfv_create">SFV_CREATE</a>



<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex">SHCreateShellFolderViewEx</a>
