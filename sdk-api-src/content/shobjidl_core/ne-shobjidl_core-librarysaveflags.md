---
UID: NE:shobjidl_core.LIBRARYSAVEFLAGS
title: LIBRARYSAVEFLAGS (shobjidl_core.h)
description: Specifies the options for handling a name collision when saving a library.
helpviewer_keywords: ["LIBRARYSAVEFLAGS","LIBRARYSAVEFLAGS enumeration [Windows Shell]","LSF_FAILIFTHERE","LSF_MAKEUNIQUENAME","LSF_OVERRIDEEXISTING","_shell_LIBRARYSAVEFLAGS","shell.LIBRARYSAVEFLAGS","shobjidl_core/LIBRARYSAVEFLAGS","shobjidl_core/LSF_FAILIFTHERE","shobjidl_core/LSF_MAKEUNIQUENAME","shobjidl_core/LSF_OVERRIDEEXISTING"]
old-location: shell\LIBRARYSAVEFLAGS.htm
tech.root: shell
ms.assetid: cae52226-0030-457b-aebf-00aaf860243d
ms.date: 12/05/2018
ms.keywords: LIBRARYSAVEFLAGS, LIBRARYSAVEFLAGS enumeration [Windows Shell], LSF_FAILIFTHERE, LSF_MAKEUNIQUENAME, LSF_OVERRIDEEXISTING, _shell_LIBRARYSAVEFLAGS, shell.LIBRARYSAVEFLAGS, shobjidl_core/LIBRARYSAVEFLAGS, shobjidl_core/LSF_FAILIFTHERE, shobjidl_core/LSF_MAKEUNIQUENAME, shobjidl_core/LSF_OVERRIDEEXISTING
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
req.typenames: LIBRARYSAVEFLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LIBRARYSAVEFLAGS
 - shobjidl_core/LIBRARYSAVEFLAGS
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
 - LIBRARYSAVEFLAGS
---

# LIBRARYSAVEFLAGS enumeration


## -description

Specifies the options for handling a name collision when saving a library.

## -enum-fields

### -field LSF_FAILIFTHERE:0

If a library with the same name already exists, the save operation fails.

### -field LSF_OVERRIDEEXISTING:0x1

If a library with the same name already exists, the save operation overwrites the existing library.

### -field LSF_MAKEUNIQUENAME:0x2

If a library with the same name already exists, the save operation generates a new, unique name for the library.

## -remarks

<h3><a id="Used_By"></a><a id="used_by"></a><a id="USED_BY"></a>Used By</h3>
<ul>
<li>
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-save">IShellLibrary::Save</a>
</li>
<li>
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-saveinknownfolder">IShellLibrary::SaveInKnownFolder</a>
</li>
<li>
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shsavelibraryinfolderpath">SHSaveLibraryInFolderPath</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a>
