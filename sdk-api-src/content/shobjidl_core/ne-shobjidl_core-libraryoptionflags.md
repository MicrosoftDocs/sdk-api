---
UID: NE:shobjidl_core.LIBRARYOPTIONFLAGS
title: LIBRARYOPTIONFLAGS (shobjidl_core.h)
description: Specifies the library options.
helpviewer_keywords: ["LIBRARYOPTIONFLAGS","LIBRARYOPTIONFLAGS enumeration [Windows Shell]","LOF_DEFAULT","LOF_MASK_ALL","LOF_PINNEDTONAVPANE","_shell_LIBRARYOPTIONFLAGS","shell.LIBRARYOPTIONFLAGS","shobjidl_core/LIBRARYOPTIONFLAGS","shobjidl_core/LOF_DEFAULT","shobjidl_core/LOF_MASK_ALL","shobjidl_core/LOF_PINNEDTONAVPANE"]
old-location: shell\LIBRARYOPTIONFLAGS.htm
tech.root: shell
ms.assetid: 205c40ff-a4dc-4a57-b51a-1e230fc170dd
ms.date: 12/05/2018
ms.keywords: LIBRARYOPTIONFLAGS, LIBRARYOPTIONFLAGS enumeration [Windows Shell], LOF_DEFAULT, LOF_MASK_ALL, LOF_PINNEDTONAVPANE, _shell_LIBRARYOPTIONFLAGS, shell.LIBRARYOPTIONFLAGS, shobjidl_core/LIBRARYOPTIONFLAGS, shobjidl_core/LOF_DEFAULT, shobjidl_core/LOF_MASK_ALL, shobjidl_core/LOF_PINNEDTONAVPANE
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
req.typenames: LIBRARYOPTIONFLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LIBRARYOPTIONFLAGS
 - shobjidl_core/LIBRARYOPTIONFLAGS
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
 - LIBRARYOPTIONFLAGS
---

# LIBRARYOPTIONFLAGS enumeration


## -description

Specifies the library options.

## -enum-fields

### -field LOF_DEFAULT:0

No library options are set.

### -field LOF_PINNEDTONAVPANE:0x1

Pin the library to the navigation pane.

### -field LOF_MASK_ALL:0x1

All valid library options flags.

## -remarks

<h3><a id="Used_By"></a><a id="used_by"></a><a id="USED_BY"></a>Used By</h3>
<ul>
<li>
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-getoptions">IShellLibrary::GetOptions</a>
</li>
<li>
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-setoptions">IShellLibrary::SetOptions</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a>
