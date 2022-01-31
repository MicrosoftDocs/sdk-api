---
UID: NE:shlwapi.__unnamed_enum_4
title: SHREGENUM_FLAGS (shlwapi.h)
description: Provides a set of values that indicate the base key that will be used for an enumeration.
helpviewer_keywords: ["SHREGENUM_BOTH","SHREGENUM_DEFAULT","SHREGENUM_FLAGS","SHREGENUM_FLAGS enumeration [Windows Shell]","SHREGENUM_HKCU","SHREGENUM_HKLM","_win32_SHREGENUM_FLAGS","shell.SHREGENUM_FLAGS","shlwapi/SHREGENUM_BOTH","shlwapi/SHREGENUM_DEFAULT","shlwapi/SHREGENUM_FLAGS","shlwapi/SHREGENUM_HKCU","shlwapi/SHREGENUM_HKLM"]
old-location: shell\SHREGENUM_FLAGS.htm
tech.root: shell
ms.assetid: 4216a983-9d53-44b1-8273-e5a90ac4b3ef
ms.date: 12/05/2018
ms.keywords: SHREGENUM_BOTH, SHREGENUM_DEFAULT, SHREGENUM_FLAGS, SHREGENUM_FLAGS enumeration [Windows Shell], SHREGENUM_HKCU, SHREGENUM_HKLM, _win32_SHREGENUM_FLAGS, shell.SHREGENUM_FLAGS, shlwapi/SHREGENUM_BOTH, shlwapi/SHREGENUM_DEFAULT, shlwapi/SHREGENUM_FLAGS, shlwapi/SHREGENUM_HKCU, shlwapi/SHREGENUM_HKLM
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
req.typenames: SHREGENUM_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHREGENUM_FLAGS
 - shlwapi/SHREGENUM_FLAGS
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
 - SHREGENUM_FLAGS
---

# SHREGENUM_FLAGS enumeration


## -description

Provides a set of values that indicate the base key that will be used for an enumeration.

## -enum-fields

### -field SHREGENUM_DEFAULT:0x00000000

Enumerates under <b>HKEY_CURRENT_USER</b>, or, if the specified item is not found in <b>HKEY_CURRENT_USER</b>, enumerates under <b>HKEY_LOCAL_MACHINE</b>.

### -field SHREGENUM_HKCU:0x00000001

Enumerates under <b>HKEY_CURRENT_USER</b> only.

### -field SHREGENUM_HKLM:0x00000010

Enumerates under <b>HKEY_LOCAL_MACHINE</b> only.

### -field SHREGENUM_BOTH:0x00000011

Not used.

