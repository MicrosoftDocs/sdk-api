---
UID: NF:shobjidl_core.IShellLibrary.SetDefaultSaveFolder
title: IShellLibrary::SetDefaultSaveFolder (shobjidl_core.h)
description: Sets the default target folder that the library will use for save operations.
helpviewer_keywords: ["IShellLibrary interface [Windows Shell]","SetDefaultSaveFolder method","IShellLibrary.SetDefaultSaveFolder","IShellLibrary::SetDefaultSaveFolder","SetDefaultSaveFolder","SetDefaultSaveFolder method [Windows Shell]","SetDefaultSaveFolder method [Windows Shell]","IShellLibrary interface","_shell_IShellLibrary_SetDefaultSaveFolder","shell.IShellLibrary_SetDefaultSaveFolder","shobjidl_core/IShellLibrary::SetDefaultSaveFolder"]
old-location: shell\IShellLibrary_SetDefaultSaveFolder.htm
tech.root: shell
ms.assetid: 0c65bd5e-22f4-450b-a1d5-75e564854b5f
ms.date: 12/05/2018
ms.keywords: IShellLibrary interface [Windows Shell],SetDefaultSaveFolder method, IShellLibrary.SetDefaultSaveFolder, IShellLibrary::SetDefaultSaveFolder, SetDefaultSaveFolder, SetDefaultSaveFolder method [Windows Shell], SetDefaultSaveFolder method [Windows Shell],IShellLibrary interface, _shell_IShellLibrary_SetDefaultSaveFolder, shell.IShellLibrary_SetDefaultSaveFolder, shobjidl_core/IShellLibrary::SetDefaultSaveFolder
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
 - IShellLibrary::SetDefaultSaveFolder
 - shobjidl_core/IShellLibrary::SetDefaultSaveFolder
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
 - IShellLibrary.SetDefaultSaveFolder
---

# IShellLibrary::SetDefaultSaveFolder


## -description

Sets the default target folder that the library will use for save operations.

## -parameters

### -param dsft [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-defaultsavefoldertype">DEFAULTSAVEFOLDERTYPE</a></b>

The <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-defaultsavefoldertype">DEFAULTSAVEFOLDERTYPE</a>  value  that specifies the default save location to set.

### -param psi [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

An  <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> object that represents the folder that to use as the default save location. The folder that this object represents must be a folder that is already in the library.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The default save location must be valid, have read/write access, and with either the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof">SFGAO_STREAM</a> or <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof">SFGAO_FILESYSTEM</a> attribute set.

If <i>psi</i> is not in the library, this method returns an error.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a>



<a href="/windows/desktop/shell/library-schema-entry">Library Description Schema</a>



<a href="/previous-versions/windows/desktop/legacy/dd758096(v=vs.85)">Windows Libraries</a>