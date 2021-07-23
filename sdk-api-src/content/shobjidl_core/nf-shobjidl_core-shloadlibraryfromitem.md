---
UID: NF:shobjidl_core.SHLoadLibraryFromItem
title: SHLoadLibraryFromItem function (shobjidl_core.h)
description: Creates and loads an IShellLibrary object from a specified library definition file.
helpviewer_keywords: ["SHLoadLibraryFromItem","SHLoadLibraryFromItem function [Windows Shell]","_shell_SHLoadLibraryFromItem","shell.SHLoadLibraryFromItem","shobjidl_core/SHLoadLibraryFromItem"]
old-location: shell\SHLoadLibraryFromItem.htm
tech.root: shell
ms.assetid: 9692f9d1-1504-43d0-9eb1-3759a8e2b42d
ms.date: 12/05/2018
ms.keywords: SHLoadLibraryFromItem, SHLoadLibraryFromItem function [Windows Shell], _shell_SHLoadLibraryFromItem, shell.SHLoadLibraryFromItem, shobjidl_core/SHLoadLibraryFromItem
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHLoadLibraryFromItem
 - shobjidl_core/SHLoadLibraryFromItem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - SHLoadLibraryFromItem
---

# SHLoadLibraryFromItem function


## -description

Creates and loads an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a> object from a specified library definition file.

## -parameters

### -param psiLibrary [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

An <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> object for the library definition file to load.

### -param grfMode [in]

Type: <b>DWORD</b>

One or more storage medium flags that specify access and sharing modes for the library object. Commonly specified flags are <b>STGM_READ</b> or <b>STGM_READWRITE</b>. For more information, see <a href="/windows/desktop/Stg/stgm-constants">STGM</a>.

### -param riid [in]

Type: <b>REFIID</b>

The IID for <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a>. (See usage remarks.)

### -param ppv [out]

Type: <b>void**</b>

Receives the loaded <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a> object. (See usage remarks.)

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<h3><a id="Usage"></a><a id="usage"></a><a id="USAGE"></a>Usage</h3>
The <b>IID_PPV_ARGS</b> macro is generally used to generate the <i>riid</i> and <i>ppv</i> parameters for this function. For an example, see <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreatelibrary">SHCreateLibrary</a>.

This is an inline helper function that wraps the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-loadlibraryfromitem">IShellLibrary::LoadLibraryFromItem</a> method.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-loadlibraryfromitem">IShellLibrary::LoadLibraryFromItem</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-loadlibraryfromknownfolder">IShellLibrary::LoadLibraryFromKnownFolder</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemwithparent">SHCreateItemWithParent</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreatelibrary">SHCreateLibrary</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetitemfromobject">SHGetItemFromObject</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shloadlibraryfromknownfolder">SHLoadLibraryFromKnownFolder</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shloadlibraryfromparsingname">SHLoadLibraryFromParsingName</a>