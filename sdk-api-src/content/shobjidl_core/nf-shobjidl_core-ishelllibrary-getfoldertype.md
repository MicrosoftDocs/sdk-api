---
UID: NF:shobjidl_core.IShellLibrary.GetFolderType
title: IShellLibrary::GetFolderType (shobjidl_core.h)
description: Gets the library's folder type.
helpviewer_keywords: ["GetFolderType","GetFolderType method [Windows Shell]","GetFolderType method [Windows Shell]","IShellLibrary interface","IShellLibrary interface [Windows Shell]","GetFolderType method","IShellLibrary.GetFolderType","IShellLibrary::GetFolderType","_shell_IShellLibrary_GetFolderType","shell.IShellLibrary_GetFolderType","shobjidl_core/IShellLibrary::GetFolderType"]
old-location: shell\IShellLibrary_GetFolderType.htm
tech.root: shell
ms.assetid: 450ee4cc-5a09-4f14-832a-3982ec9de03b
ms.date: 12/05/2018
ms.keywords: GetFolderType, GetFolderType method [Windows Shell], GetFolderType method [Windows Shell],IShellLibrary interface, IShellLibrary interface [Windows Shell],GetFolderType method, IShellLibrary.GetFolderType, IShellLibrary::GetFolderType, _shell_IShellLibrary_GetFolderType, shell.IShellLibrary_GetFolderType, shobjidl_core/IShellLibrary::GetFolderType
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
 - IShellLibrary::GetFolderType
 - shobjidl_core/IShellLibrary::GetFolderType
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
 - IShellLibrary.GetFolderType
---

# IShellLibrary::GetFolderType


## -description

Gets the library's folder type.

## -parameters

### -param pftid [out]

Type: <b><a href="/windows/desktop/shell/foldertypeid">FOLDERTYPEID</a>*</b>

The  view template that is applied to a folder, usually based on its intended use and contents.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The folder type determines the default view template that is used by the folder. A view template specifies the columns and details that appear by default in the Windows Explorer view of the folder.


<a href="/windows/desktop/shell/foldertypeid">FOLDERTYPEID</a> values are GUID  values that are defined in shlguid.h.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a>



<a href="/windows/desktop/shell/library-schema-entry">Library Description Schema</a>



<a href="/previous-versions/windows/desktop/legacy/dd758096(v=vs.85)">Windows Libraries</a>



<a href="/previous-versions/windows/desktop/legacy/dd798386(v=vs.85)">folderType Element (Library Schema)</a>