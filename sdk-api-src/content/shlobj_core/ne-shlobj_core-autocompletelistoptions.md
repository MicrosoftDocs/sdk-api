---
UID: NE:shlobj_core._tagAUTOCOMPLETELISTOPTIONS
title: AUTOCOMPLETELISTOPTIONS (shlobj_core.h)
description: Specifies which objects are enumerated for autocompletion lists.
helpviewer_keywords: ["ACLO_CURRENTDIR","ACLO_DESKTOP","ACLO_FAVORITES","ACLO_FILESYSDIRS","ACLO_FILESYSONLY","ACLO_MYCOMPUTER","ACLO_NONE","ACLO_VIRTUALNAMESPACE","AUTOCOMPLETELISTOPTIONS","AUTOCOMPLETELISTOPTIONS enumeration [Windows Shell]","_shell_AUTOCOMPLETELISTOPTIONS","shell.AUTOCOMPLETELISTOPTIONS","shlobj_core/ACLO_CURRENTDIR","shlobj_core/ACLO_DESKTOP","shlobj_core/ACLO_FAVORITES","shlobj_core/ACLO_FILESYSDIRS","shlobj_core/ACLO_FILESYSONLY","shlobj_core/ACLO_MYCOMPUTER","shlobj_core/ACLO_NONE","shlobj_core/ACLO_VIRTUALNAMESPACE","shlobj_core/AUTOCOMPLETELISTOPTIONS"]
old-location: shell\AUTOCOMPLETELISTOPTIONS.htm
tech.root: shell
ms.assetid: 9bcd031c-afcd-4e3d-97d0-fb2095f9d0fc
ms.date: 12/05/2018
ms.keywords: ACLO_CURRENTDIR, ACLO_DESKTOP, ACLO_FAVORITES, ACLO_FILESYSDIRS, ACLO_FILESYSONLY, ACLO_MYCOMPUTER, ACLO_NONE, ACLO_VIRTUALNAMESPACE, AUTOCOMPLETELISTOPTIONS, AUTOCOMPLETELISTOPTIONS enumeration [Windows Shell], _shell_AUTOCOMPLETELISTOPTIONS, shell.AUTOCOMPLETELISTOPTIONS, shlobj_core/ACLO_CURRENTDIR, shlobj_core/ACLO_DESKTOP, shlobj_core/ACLO_FAVORITES, shlobj_core/ACLO_FILESYSDIRS, shlobj_core/ACLO_FILESYSONLY, shlobj_core/ACLO_MYCOMPUTER, shlobj_core/ACLO_NONE, shlobj_core/ACLO_VIRTUALNAMESPACE, shlobj_core/AUTOCOMPLETELISTOPTIONS
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: AUTOCOMPLETELISTOPTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _tagAUTOCOMPLETELISTOPTIONS
 - shlobj_core/_tagAUTOCOMPLETELISTOPTIONS
 - AUTOCOMPLETELISTOPTIONS
 - shlobj_core/AUTOCOMPLETELISTOPTIONS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - AUTOCOMPLETELISTOPTIONS
---

# AUTOCOMPLETELISTOPTIONS enumeration


## -description

Specifies which objects are enumerated for autocompletion lists.

## -enum-fields

### -field ACLO_NONE:0

No enumeration should take place.

### -field ACLO_CURRENTDIR:1

Only the current directory should be enumerated.

### -field ACLO_MYCOMPUTER:2

Only MyComputer should be enumerated.

### -field ACLO_DESKTOP:4

Only the Desktop Folder should be enumerated.

### -field ACLO_FAVORITES:8

Only the Favorites Folder should be enumerated.

### -field ACLO_FILESYSONLY:16

Only the file system should be enumerated.

### -field ACLO_FILESYSDIRS:32

<b>Internet Explorer 6 or greater:</b> The file system dirs, UNC shares, and UNC servers should be enumerated.

### -field ACLO_VIRTUALNAMESPACE:64

<b>Windows Internet Explorer 7 or greater:</b> The virtual namespace should be enumerated.

