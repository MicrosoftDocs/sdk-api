---
UID: NF:shobjidl_core.IShellLibrary.GetDefaultSaveFolder
title: IShellLibrary::GetDefaultSaveFolder (shobjidl_core.h)
description: Retrieves the default target folder that the library uses for save operations.
helpviewer_keywords: ["GetDefaultSaveFolder","GetDefaultSaveFolder method [Windows Shell]","GetDefaultSaveFolder method [Windows Shell]","IShellLibrary interface","IShellLibrary interface [Windows Shell]","GetDefaultSaveFolder method","IShellLibrary.GetDefaultSaveFolder","IShellLibrary::GetDefaultSaveFolder","_shell_IShellLibrary_GetDefaultSaveFolder","shell.IShellLibrary_GetDefaultSaveFolder","shobjidl_core/IShellLibrary::GetDefaultSaveFolder"]
old-location: shell\IShellLibrary_GetDefaultSaveFolder.htm
tech.root: shell
ms.assetid: 4bc501b1-2fc4-49ce-a16b-e254a3a40f46
ms.date: 12/05/2018
ms.keywords: GetDefaultSaveFolder, GetDefaultSaveFolder method [Windows Shell], GetDefaultSaveFolder method [Windows Shell],IShellLibrary interface, IShellLibrary interface [Windows Shell],GetDefaultSaveFolder method, IShellLibrary.GetDefaultSaveFolder, IShellLibrary::GetDefaultSaveFolder, _shell_IShellLibrary_GetDefaultSaveFolder, shell.IShellLibrary_GetDefaultSaveFolder, shobjidl_core/IShellLibrary::GetDefaultSaveFolder
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
 - IShellLibrary::GetDefaultSaveFolder
 - shobjidl_core/IShellLibrary::GetDefaultSaveFolder
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
 - IShellLibrary.GetDefaultSaveFolder
---

# IShellLibrary::GetDefaultSaveFolder


## -description

Retrieves the default target folder that the library uses  for save operations.

## -parameters

### -param dsft [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-defaultsavefoldertype">DEFAULTSAVEFOLDERTYPE</a></b>

The <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-defaultsavefoldertype">DEFAULTSAVEFOLDERTYPE</a>  value that specifies the save folder to get.

### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to get in <i>ppv</i> that will represent the save location.   This value is typically IID_IShellItem,  but it can also be IID_IShellItem2 or the IID of any other interface that is implemented by CShellItem.

### -param ppv [out]

Type: <b>void**</b>

A  pointer  to the interface requested in <i>riid</i>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For best results, use the <b>IID_PPV_ARGS</b> macro, defined in Objbase.h,  for  the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem2">IShellItem2</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a>



<a href="/windows/desktop/shell/library-schema-entry">Library Description Schema</a>



<a href="/previous-versions/windows/desktop/legacy/dd758096(v=vs.85)">Windows Libraries</a>