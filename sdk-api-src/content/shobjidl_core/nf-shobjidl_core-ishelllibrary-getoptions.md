---
UID: NF:shobjidl_core.IShellLibrary.GetOptions
title: IShellLibrary::GetOptions (shobjidl_core.h)
description: Gets the library's options.
helpviewer_keywords: ["GetOptions","GetOptions method [Windows Shell]","GetOptions method [Windows Shell]","IShellLibrary interface","IShellLibrary interface [Windows Shell]","GetOptions method","IShellLibrary.GetOptions","IShellLibrary::GetOptions","_shell_IShellLibrary_GetOptions","shell.IShellLibrary_GetOptions","shobjidl_core/IShellLibrary::GetOptions"]
old-location: shell\IShellLibrary_GetOptions.htm
tech.root: shell
ms.assetid: 1a144505-e977-4db6-8266-c39c1de8a8f9
ms.date: 12/05/2018
ms.keywords: GetOptions, GetOptions method [Windows Shell], GetOptions method [Windows Shell],IShellLibrary interface, IShellLibrary interface [Windows Shell],GetOptions method, IShellLibrary.GetOptions, IShellLibrary::GetOptions, _shell_IShellLibrary_GetOptions, shell.IShellLibrary_GetOptions, shobjidl_core/IShellLibrary::GetOptions
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - IShellLibrary::GetOptions
 - shobjidl_core/IShellLibrary::GetOptions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IShellLibrary.GetOptions
---

# IShellLibrary::GetOptions


## -description

Gets the library's options.

## -parameters

### -param plofOptions [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-libraryoptionflags">LIBRARYOPTIONFLAGS</a>*</b>

The library options for this library. <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-libraryoptionflags">LIBRARYOPTIONFLAGS</a> is a bitwise enumerator, which means that more than one flag could be set.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a>



<a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-libraryoptionflags">LIBRARYOPTIONFLAGS</a>



<a href="/windows/desktop/shell/library-schema-entry">Library Description Schema</a>



<a href="/previous-versions/windows/desktop/legacy/dd758096(v=vs.85)">Windows Libraries</a>