---
UID: NE:shobjidl_core.LIBRARYFOLDERFILTER
title: LIBRARYFOLDERFILTER (shobjidl_core.h)
description: Defines options for filtering folder items.
helpviewer_keywords: ["LFF_ALLITEMS","LFF_FORCEFILESYSTEM","LFF_STORAGEITEMS","LIBRARYFOLDERFILTER","LIBRARYFOLDERFILTER enumeration [Windows Shell]","_shell_LIBRARYFOLDERFILTER","shell.LIBRARYFOLDERFILTER","shobjidl_core/LFF_ALLITEMS","shobjidl_core/LFF_FORCEFILESYSTEM","shobjidl_core/LFF_STORAGEITEMS","shobjidl_core/LIBRARYFOLDERFILTER"]
old-location: shell\LIBRARYFOLDERFILTER.htm
tech.root: shell
ms.assetid: 8bcb8ee7-14a9-411e-978d-ddeed83d8392
ms.date: 12/05/2018
ms.keywords: LFF_ALLITEMS, LFF_FORCEFILESYSTEM, LFF_STORAGEITEMS, LIBRARYFOLDERFILTER, LIBRARYFOLDERFILTER enumeration [Windows Shell], _shell_LIBRARYFOLDERFILTER, shell.LIBRARYFOLDERFILTER, shobjidl_core/LFF_ALLITEMS, shobjidl_core/LFF_FORCEFILESYSTEM, shobjidl_core/LFF_STORAGEITEMS, shobjidl_core/LIBRARYFOLDERFILTER
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
req.typenames: LIBRARYFOLDERFILTER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LIBRARYFOLDERFILTER
 - shobjidl_core/LIBRARYFOLDERFILTER
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
 - LIBRARYFOLDERFILTER
---

# LIBRARYFOLDERFILTER enumeration


## -description

Defines options for filtering folder items.

## -enum-fields

### -field LFF_FORCEFILESYSTEM:1

Return only file system items.

### -field LFF_STORAGEITEMS:2

Return items that can be bound to an IStorage object.

### -field LFF_ALLITEMS:3

Return all items.

## -remarks

<h3><a id="Used_By"></a><a id="used_by"></a><a id="USED_BY"></a>Used By</h3>
The <b>LIBRARYFOLDERFILTER</b> enumeration is used by the following methods and functions.
         

<ul>
<li>
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-getfolders">IShellLibrary::GetFolders</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a>
