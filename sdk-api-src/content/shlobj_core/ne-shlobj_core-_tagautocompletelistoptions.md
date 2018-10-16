---
UID: NE:shlobj_core._tagAUTOCOMPLETELISTOPTIONS
title: "_tagAUTOCOMPLETELISTOPTIONS"
author: windows-sdk-content
description: Specifies which objects are enumerated for autocompletion lists.
old-location: shell\AUTOCOMPLETELISTOPTIONS.htm
tech.root: shell
ms.assetid: 9bcd031c-afcd-4e3d-97d0-fb2095f9d0fc
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: ACLO_CURRENTDIR, ACLO_DESKTOP, ACLO_FAVORITES, ACLO_FILESYSDIRS, ACLO_FILESYSONLY, ACLO_MYCOMPUTER, ACLO_NONE, ACLO_VIRTUALNAMESPACE, AUTOCOMPLETELISTOPTIONS, AUTOCOMPLETELISTOPTIONS enumeration [Windows Shell], _shell_AUTOCOMPLETELISTOPTIONS, _tagAUTOCOMPLETELISTOPTIONS, shell.AUTOCOMPLETELISTOPTIONS, shlobj_core/ACLO_CURRENTDIR, shlobj_core/ACLO_DESKTOP, shlobj_core/ACLO_FAVORITES, shlobj_core/ACLO_FILESYSDIRS, shlobj_core/ACLO_FILESYSONLY, shlobj_core/ACLO_MYCOMPUTER, shlobj_core/ACLO_NONE, shlobj_core/ACLO_VIRTUALNAMESPACE, shlobj_core/AUTOCOMPLETELISTOPTIONS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - AUTOCOMPLETELISTOPTIONS
product: Windows
targetos: Windows
req.typenames: AUTOCOMPLETELISTOPTIONS
req.redist: 
---

# _tagAUTOCOMPLETELISTOPTIONS enumeration


## -description


Specifies which objects are enumerated for autocompletion lists.


## -enum-fields




### -field ACLO_NONE

No enumeration should take place.


### -field ACLO_CURRENTDIR

Only the current directory should be enumerated.


### -field ACLO_MYCOMPUTER

Only MyComputer should be enumerated.


### -field ACLO_DESKTOP

Only the Desktop Folder should be enumerated.


### -field ACLO_FAVORITES

Only the Favorites Folder should be enumerated.


### -field ACLO_FILESYSONLY

Only the file system should be enumerated.


### -field ACLO_FILESYSDIRS

<b>Internet Explorer 6 or greater:</b> The file system dirs, UNC shares, and UNC servers should be enumerated.


### -field ACLO_VIRTUALNAMESPACE

<b>Windows Internet Explorer 7 or greater:</b> The virtual namespace should be enumerated.

