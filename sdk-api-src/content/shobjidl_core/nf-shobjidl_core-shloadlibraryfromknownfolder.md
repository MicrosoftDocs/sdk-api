---
UID: NF:shobjidl_core.SHLoadLibraryFromKnownFolder
title: SHLoadLibraryFromKnownFolder function (shobjidl_core.h)
description: Creates and loads an IShellLibrary object for a specified known folder ID.
helpviewer_keywords: ["SHLoadLibraryFromKnownFolder","SHLoadLibraryFromKnownFolder function [Windows Shell]","_shell_SHLoadLibraryFromKnownFolder","shell.SHLoadLibraryFromKnownFolder","shobjidl_core/SHLoadLibraryFromKnownFolder"]
old-location: shell\SHLoadLibraryFromKnownFolder.htm
tech.root: shell
ms.assetid: 9486252b-9aaf-4daf-b307-5a5adddfaa99
ms.date: 12/05/2018
ms.keywords: SHLoadLibraryFromKnownFolder, SHLoadLibraryFromKnownFolder function [Windows Shell], _shell_SHLoadLibraryFromKnownFolder, shell.SHLoadLibraryFromKnownFolder, shobjidl_core/SHLoadLibraryFromKnownFolder
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
 - SHLoadLibraryFromKnownFolder
 - shobjidl_core/SHLoadLibraryFromKnownFolder
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
 - SHLoadLibraryFromKnownFolder
---

# SHLoadLibraryFromKnownFolder function


## -description

Creates and loads an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a> object for a specified known folder ID.

## -parameters

### -param kfidLibrary [in]

Type: <b>REFKNOWNFOLDERID</b>

The <a href="/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a> value that identifies the known folder to load into the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a> object.

### -param grfMode [in]

Type: <b>DWORD</b>

One or more storage medium flags that specify access and sharing modes for the library object. Commonly specified flags are <b>STGM_READ</b> or <b>STGM_READWRITE</b>. For more information, see <a href="/windows/desktop/Stg/stgm-constants">STGM</a>.

### -param riid [in]

Type: <b>REFIID</b>

The IID for <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a>. (See Remarks for more information.)

### -param ppv [out]

Type: <b>void**</b>

When this function returns successfully, receives the loaded <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a> object. (See Remarks for more information.)

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is an inline helper function that wraps the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-loadlibraryfromknownfolder">IShellLibrary::LoadLibraryFromKnownFolder</a> method.

<h3><a id="Usage"></a><a id="usage"></a><a id="USAGE"></a>Usage</h3>
The <b>IID_PPV_ARGS</b> macro is generally used to generate the <i>riid</i> and <i>ppv</i> parameters for this function. For an example, see <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreatelibrary">SHCreateLibrary</a>.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-loadlibraryfromitem">IShellLibrary::LoadLibraryFromItem</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-loadlibraryfromknownfolder">IShellLibrary::LoadLibraryFromKnownFolder</a>



<a href="/previous-versions/windows/desktop/legacy/dd940364(v=vs.85)">Known Folders Sample</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreatelibrary">SHCreateLibrary</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shloadlibraryfromitem">SHLoadLibraryFromItem</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shloadlibraryfromparsingname">SHLoadLibraryFromParsingName</a>