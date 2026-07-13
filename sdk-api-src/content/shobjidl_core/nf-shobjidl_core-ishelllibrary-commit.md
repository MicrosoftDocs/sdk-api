---
UID: NF:shobjidl_core.IShellLibrary.Commit
title: IShellLibrary::Commit (shobjidl_core.h)
description: Commits library updates to an existing Library Description file.
helpviewer_keywords: ["Commit","Commit method [Windows Shell]","Commit method [Windows Shell]","IShellLibrary interface","IShellLibrary interface [Windows Shell]","Commit method","IShellLibrary.Commit","IShellLibrary::Commit","_shell_IShellLibrary_Commit","shell.IShellLibrary_Commit","shobjidl_core/IShellLibrary::Commit"]
old-location: shell\IShellLibrary_Commit.htm
tech.root: shell
ms.assetid: a340964d-ea20-4a3b-be8b-f4f4dbf624ed
ms.date: 12/05/2018
ms.keywords: Commit, Commit method [Windows Shell], Commit method [Windows Shell],IShellLibrary interface, IShellLibrary interface [Windows Shell],Commit method, IShellLibrary.Commit, IShellLibrary::Commit, _shell_IShellLibrary_Commit, shell.IShellLibrary_Commit, shobjidl_core/IShellLibrary::Commit
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
 - IShellLibrary::Commit
 - shobjidl_core/IShellLibrary::Commit
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
 - IShellLibrary.Commit
---

# IShellLibrary::Commit


## -description

Commits library updates to an existing Library Description file.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>IShellLibrary::Commit</b>  can only be called to save library updates to an existing file.  A call to <b>IShellLibrary::Commit</b> for a library that does not have a backing file will fail.
         
To create and save a new file, call  <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-save">IShellLibrary::Save</a> or <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shsavelibraryinfolderpath">SHSaveLibraryInFolderPath</a>.
         

If the library is saved in the Libraries known folder (FOLDERID_Libraries), the folders in the library are automatically added to the search index.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-save">IShellLibrary::Save</a>



<a href="/windows/desktop/shell/library-schema-entry">Library Description Schema</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shsavelibraryinfolderpath">SHSaveLibraryInFolderPath</a>



<a href="/previous-versions/windows/desktop/legacy/dd758096(v=vs.85)">Windows Libraries</a>
