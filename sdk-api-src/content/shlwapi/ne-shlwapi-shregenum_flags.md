---
UID: NE:shlwapi.SHREGENUM_FLAGS
title: SHREGENUM_FLAGS
author: windows-sdk-content
description: Provides a set of values that indicate the base key that will be used for an enumeration.
old-location: shell\SHREGENUM_FLAGS.htm
old-project: shell
ms.assetid: 4216a983-9d53-44b1-8273-e5a90ac4b3ef
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: SHREGENUM_BOTH, SHREGENUM_DEFAULT, SHREGENUM_FLAGS, SHREGENUM_FLAGS enumeration [Windows Shell], SHREGENUM_HKCU, SHREGENUM_HKLM, _win32_SHREGENUM_FLAGS, shell.SHREGENUM_FLAGS, shlwapi/SHREGENUM_BOTH, shlwapi/SHREGENUM_DEFAULT, shlwapi/SHREGENUM_FLAGS, shlwapi/SHREGENUM_HKCU, shlwapi/SHREGENUM_HKLM
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: SHREGENUM_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shlwapi.h
api_name:
 - SHREGENUM_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# SHREGENUM_FLAGS enumeration


## -description


Provides a set of values that indicate the base key that will be used for an enumeration.


## -enum-fields




### -field SHREGENUM_DEFAULT

Enumerates under <b>HKEY_CURRENT_USER</b>, or, if the specified item is not found in <b>HKEY_CURRENT_USER</b>, enumerates under <b>HKEY_LOCAL_MACHINE</b>.


### -field SHREGENUM_HKCU

Enumerates under <b>HKEY_CURRENT_USER</b> only.


### -field SHREGENUM_HKLM

Enumerates under <b>HKEY_LOCAL_MACHINE</b> only.


### -field SHREGENUM_BOTH

Not used.

