---
UID: NF:shobjidl_core.SHLoadLibraryFromParsingName
title: SHLoadLibraryFromParsingName function (shobjidl_core.h)
description: Creates and loads an IShellLibrary object for a specified path.
helpviewer_keywords: ["SHLoadLibraryFromParsingName","SHLoadLibraryFromParsingName function [Windows Shell]","_shell_SHLoadLibraryFromParsingName","shell.SHLoadLibraryFromParsingName","shobjidl_core/SHLoadLibraryFromParsingName"]
old-location: shell\SHLoadLibraryFromParsingName.htm
tech.root: shell
ms.assetid: 49433938-d31e-49f8-9dc7-3df5fb3bfcad
ms.date: 12/05/2018
ms.keywords: SHLoadLibraryFromParsingName, SHLoadLibraryFromParsingName function [Windows Shell], _shell_SHLoadLibraryFromParsingName, shell.SHLoadLibraryFromParsingName, shobjidl_core/SHLoadLibraryFromParsingName
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
 - SHLoadLibraryFromParsingName
 - shobjidl_core/SHLoadLibraryFromParsingName
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
 - SHLoadLibraryFromParsingName
---

# SHLoadLibraryFromParsingName function


## -description

Creates and loads an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a> object for a specified path.

## -parameters

### -param pszParsingName [in]

Type: <b>PCWSTR</b>

The path for which to load the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a> object.

### -param grfMode [in]

Type: <b>DWORD</b>

One or more storage medium flags that specify access and sharing modes for the library object. Commonly specified flags are <b>STGM_READ</b> or <b>STGM_READWRITE</b>. For more information, see <a href="/windows/desktop/Stg/stgm-constants">STGM</a>.

### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to retrieve through <i>ppv</i>, typically IID_IShellLibrary.

### -param ppv [out]

Type: <b>void**</b>

When this method returns successfully, contains the interface pointer requested in <i>riid</i>. This is typically <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

We recommend that you use the <b>IID_PPV_ARGS</b> macro, defined in Objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error in <i>riid</i> that could lead to unexpected results.

This is an inline helper function that wraps the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-loadlibraryfromitem">IShellLibrary::LoadLibraryFromItem</a> method.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-loadlibraryfromitem">IShellLibrary::LoadLibraryFromItem</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-loadlibraryfromknownfolder">IShellLibrary::LoadLibraryFromKnownFolder</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreatelibrary">SHCreateLibrary</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shloadlibraryfromitem">SHLoadLibraryFromItem</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shloadlibraryfromknownfolder">SHLoadLibraryFromKnownFolder</a>