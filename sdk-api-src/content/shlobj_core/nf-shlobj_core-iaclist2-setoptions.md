---
UID: NF:shlobj_core.IACList2.SetOptions
title: IACList2::SetOptions (shlobj_core.h)
description: Sets the current autocomplete options. (IACList2.SetOptions)
helpviewer_keywords: ["ACLO_CURRENTDIR","ACLO_DESKTOP","ACLO_FAVORITES","ACLO_FILESYSDIRS","ACLO_FILESYSONLY","ACLO_MYCOMPUTER","ACLO_NONE","IACList2 interface [Windows Shell]","SetOptions method","IACList2.SetOptions","IACList2::SetOptions","SetOptions","SetOptions method [Windows Shell]","SetOptions method [Windows Shell]","IACList2 interface","_win32_IACList2_SetOptions","shell.IACList2_SetOptions","shlobj_core/IACList2::SetOptions"]
old-location: shell\IACList2_SetOptions.htm
tech.root: shell
ms.assetid: 963428b3-408f-4bdd-b230-9e73f21247a7
ms.date: 12/05/2018
ms.keywords: ACLO_CURRENTDIR, ACLO_DESKTOP, ACLO_FAVORITES, ACLO_FILESYSDIRS, ACLO_FILESYSONLY, ACLO_MYCOMPUTER, ACLO_NONE, IACList2 interface [Windows Shell],SetOptions method, IACList2.SetOptions, IACList2::SetOptions, SetOptions, SetOptions method [Windows Shell], SetOptions method [Windows Shell],IACList2 interface, _win32_IACList2_SetOptions, shell.IACList2_SetOptions, shlobj_core/IACList2::SetOptions
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IACList2::SetOptions
 - shlobj_core/IACList2::SetOptions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IACList2.SetOptions
---

# IACList2::SetOptions


## -description

Sets the current autocomplete options.

## -parameters

### -param dwFlag [in]

Type: <b>DWORD</b>

New option flags. Use these flags to ask the client to include the names of the files and subfolders of the specified folders the next time the client's <a href="/windows/desktop/api/objidl/nn-objidl-ienumstring">IEnumString</a> interface is called. This parameter can contain one or more of the following flags.



#### ACLO_CURRENTDIR

Enumerate the current working directory.



#### ACLO_DESKTOP

Enumerate the Desktop folder.



#### ACLO_FAVORITES

Enumerate the Favorites folder.



#### ACLO_FILESYSONLY

Enumerate only those items that are part of the file system. Do not enumerate items contained by virtual folders.



#### ACLO_FILESYSDIRS

Enumerate only the file system directories, UNC shares, and UNC servers.



#### ACLO_MYCOMPUTER

Enumerate the My Computer folder.



#### ACLO_NONE

Do not enumerate anything.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM error value otherwise.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iaclist2">IACList2</a>
