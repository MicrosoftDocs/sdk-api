---
UID: NE:shobjidl_core.LIBRARYMANAGEDIALOGOPTIONS
title: LIBRARYMANAGEDIALOGOPTIONS (shobjidl_core.h)
description: Used by SHShowManageLibraryUI to define options for handling a name collision when saving a library.
helpviewer_keywords: ["LIBRARYMANAGEDIALOGOPTIONS","LIBRARYMANAGEDIALOGOPTIONS enumeration [Windows Shell]","LMD_ALLOWUNINDEXABLENETWORKLOCATIONS","LMD_DEFAULT","_shell_LIBRARYMANAGEDIALOGOPTIONS","shell.LIBRARYMANAGEDIALOGOPTIONS","shobjidl_core/LIBRARYMANAGEDIALOGOPTIONS","shobjidl_core/LMD_ALLOWUNINDEXABLENETWORKLOCATIONS","shobjidl_core/LMD_DEFAULT"]
old-location: shell\LIBRARYMANAGEDIALOGOPTIONS.htm
tech.root: shell
ms.assetid: e5eaf131-9562-4ab0-a8bc-4eaaaa806a8f
ms.date: 12/05/2018
ms.keywords: LIBRARYMANAGEDIALOGOPTIONS, LIBRARYMANAGEDIALOGOPTIONS enumeration [Windows Shell], LMD_ALLOWUNINDEXABLENETWORKLOCATIONS, LMD_DEFAULT, _shell_LIBRARYMANAGEDIALOGOPTIONS, shell.LIBRARYMANAGEDIALOGOPTIONS, shobjidl_core/LIBRARYMANAGEDIALOGOPTIONS, shobjidl_core/LMD_ALLOWUNINDEXABLENETWORKLOCATIONS, shobjidl_core/LMD_DEFAULT
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
req.typenames: LIBRARYMANAGEDIALOGOPTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LIBRARYMANAGEDIALOGOPTIONS
 - shobjidl_core/LIBRARYMANAGEDIALOGOPTIONS
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
 - LIBRARYMANAGEDIALOGOPTIONS
---

# LIBRARYMANAGEDIALOGOPTIONS enumeration


## -description

Used by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shshowmanagelibraryui">SHShowManageLibraryUI</a> to define options for handling a name collision when saving a library.

## -enum-fields

### -field LMD_DEFAULT:0

Show default warning UI to the user.

### -field LMD_ALLOWUNINDEXABLENETWORKLOCATIONS:0x1

Do not display a warning dialog to the user in collisions that concern network locations that cannot be indexed.
