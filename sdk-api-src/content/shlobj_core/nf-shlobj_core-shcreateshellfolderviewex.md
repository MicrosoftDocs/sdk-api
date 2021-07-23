---
UID: NF:shlobj_core.SHCreateShellFolderViewEx
title: SHCreateShellFolderViewEx function (shlobj_core.h)
description: Creates a new instance of the default Shell folder view object. It is recommended that you use SHCreateShellFolderView rather than this function.
helpviewer_keywords: ["SHCreateShellFolderViewEx","SHCreateShellFolderViewEx function [Windows Shell]","_win32_SHCreateShellFolderViewEx","shell.SHCreateShellFolderViewEx","shlobj_core/SHCreateShellFolderViewEx"]
old-location: shell\SHCreateShellFolderViewEx.htm
tech.root: shell
ms.assetid: 7edd6786-7d74-4065-8cf1-cbb489007a46
ms.date: 12/05/2018
ms.keywords: SHCreateShellFolderViewEx, SHCreateShellFolderViewEx function [Windows Shell], _win32_SHCreateShellFolderViewEx, shell.SHCreateShellFolderViewEx, shlobj_core/SHCreateShellFolderViewEx
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
 - SHCreateShellFolderViewEx
 - shlobj_core/SHCreateShellFolderViewEx
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
 - SHCreateShellFolderViewEx
---

# SHCreateShellFolderViewEx function


## -description

Creates a new instance of the default Shell folder view object. It is recommended that you use <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview">SHCreateShellFolderView</a> rather than this function.

## -parameters

### -param pcsfv [in]

Type: <b><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-csfv">CSFV</a>*</b>

Pointer to a structure that describes the details used in creating this instance of the Shell folder view object.

### -param ppsv [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>**</b>

The address of an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> interface pointer that, when this function returns successfully, points to the new view object. On failure, this value is <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview">SHCreateShellFolderView</a> is recommended over <b>SHCreateShellFolderViewEx</b> because of the greater flexibility of its elements to participate in various scenarios, provide new functionality to the view, and interact with other objects.

When dealing with several instances of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>, you might want to verify which is the default Shell folder view object. To do so, call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on the object using IID_CDefView. This call succeeds only on the default Shell folder view object.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview">SHCreateShellFolderView</a>