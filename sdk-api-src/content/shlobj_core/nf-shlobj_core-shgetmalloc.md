---
UID: NF:shlobj_core.SHGetMalloc
title: SHGetMalloc function (shlobj_core.h)
description: Retrieves a pointer to the Shell's IMalloc interface.
helpviewer_keywords: ["SHGetMalloc","SHGetMalloc function [Windows Shell]","_win32_SHGetMalloc","shell.SHGetMalloc","shlobj_core/SHGetMalloc"]
old-location: shell\SHGetMalloc.htm
tech.root: shell
ms.assetid: 720cacb9-af54-41b7-9fb6-72dfa634c4c5
ms.date: 12/05/2018
ms.keywords: SHGetMalloc, SHGetMalloc function [Windows Shell], _win32_SHGetMalloc, shell.SHGetMalloc, shlobj_core/SHGetMalloc
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHGetMalloc
 - shlobj_core/SHGetMalloc
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
 - SHGetMalloc
---

# SHGetMalloc function


## -description

<p class="CCE_Message">[<b>SHGetMalloc</b> is available through Windows Vista and Windows Server 2003, but may be altered or unavailable in subsequent versions of the operating system or product. See the Remarks section for alternate recommendations.]

Retrieves a pointer to the Shell's <a href="/windows/desktop/api/objidl/nn-objidl-imalloc">IMalloc</a> interface.

## -parameters

### -param ppMalloc

Type: <b>LPMALLOC*</b>

The address of a pointer that receives the Shell's <a href="/windows/desktop/api/objidl/nn-objidl-imalloc">IMalloc</a> interface pointer.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>SHGetMalloc</b> was introduced in Windows 95 and Microsoft Windows NT 4.0, but as of Windows 2000 it is no longer necessary. In its place, programs can call the equivalent (and easier to use) <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> and <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>. If you find an older reference document that suggests or even requires the use of <b>SHGetMalloc</b>, it is acceptable and encouraged to use <b>CoTaskMemAlloc</b> and <b>CoTaskMemFree</b> instead.