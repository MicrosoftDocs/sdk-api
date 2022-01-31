---
UID: NE:shlwapi.__unnamed_enum_3
title: SHREGDEL_FLAGS (shlwapi.h)
description: Provides a set of values that indicate from which base key an item will be deleted.
helpviewer_keywords: ["SHREGDEL_BOTH","SHREGDEL_DEFAULT","SHREGDEL_FLAGS","SHREGDEL_FLAGS enumeration [Windows Shell]","SHREGDEL_HKCU","SHREGDEL_HKLM","_win32_SHREGDEL_FLAGS","shell.SHREGDEL_FLAGS","shlwapi/SHREGDEL_BOTH","shlwapi/SHREGDEL_DEFAULT","shlwapi/SHREGDEL_FLAGS","shlwapi/SHREGDEL_HKCU","shlwapi/SHREGDEL_HKLM"]
old-location: shell\SHREGDEL_FLAGS.htm
tech.root: shell
ms.assetid: 90a8bf22-f62b-4027-8219-7a5ead6577da
ms.date: 12/05/2018
ms.keywords: SHREGDEL_BOTH, SHREGDEL_DEFAULT, SHREGDEL_FLAGS, SHREGDEL_FLAGS enumeration [Windows Shell], SHREGDEL_HKCU, SHREGDEL_HKLM, _win32_SHREGDEL_FLAGS, shell.SHREGDEL_FLAGS, shlwapi/SHREGDEL_BOTH, shlwapi/SHREGDEL_DEFAULT, shlwapi/SHREGDEL_FLAGS, shlwapi/SHREGDEL_HKCU, shlwapi/SHREGDEL_HKLM
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: SHREGDEL_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHREGDEL_FLAGS
 - shlwapi/SHREGDEL_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shlwapi.h
api_name:
 - SHREGDEL_FLAGS
---

# SHREGDEL_FLAGS enumeration


## -description

Provides a set of values that indicate from which base key an item will be deleted.

## -enum-fields

### -field SHREGDEL_DEFAULT:0x00000000

Deletes from <b>HKEY_CURRENT_USER</b>. If the specified item is not found under <b>HKEY_CURRENT_USER</b>, deletes from <b>HKEY_LOCAL_MACHINE</b>.

### -field SHREGDEL_HKCU:0x00000001

Enumerates from <b>HKEY_CURRENT_USER</b> only.

### -field SHREGDEL_HKLM:0x00000010

Enumerates under <b>HKEY_LOCAL_MACHINE</b> only.

### -field SHREGDEL_BOTH:0x00000011

Deletes from both <b>HKEY_CURRENT_USER</b> and <b>HKEY_LOCAL_MACHINE</b>.

