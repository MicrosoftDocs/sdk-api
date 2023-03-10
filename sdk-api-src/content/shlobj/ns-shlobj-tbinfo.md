---
UID: NS:shlobj._TBINFO
title: TBINFO (shlobj.h)
description: Used with the SFVM_GETBUTTONINFO notification to specify the number of buttons to add to the toolbar, as well as how they're added.
helpviewer_keywords: ["*LPTBINFO","TBIF_APPEND","TBIF_PREPEND","TBIF_REPLACE","TBINFO","TBINFO structure [Windows Shell]","_win32_TBINFO_str","shell.TBINFO_str","shlobj/TBINFO"]
old-location: shell\TBINFO_str.htm
tech.root: shell
ms.assetid: da82e861-129b-4536-b036-2238c9e4c84c
ms.date: 12/05/2018
ms.keywords: '*LPTBINFO, TBIF_APPEND, TBIF_PREPEND, TBIF_REPLACE, TBINFO, TBINFO structure [Windows Shell], _win32_TBINFO_str, shell.TBINFO_str, shlobj/TBINFO'
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.typenames: TBINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TBINFO
 - shlobj/_TBINFO
 - TBINFO
 - shlobj/TBINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shlobj.h
api_name:
 - TBINFO
---

# TBINFO structure


## -description

Used with the <a href="/windows/desktop/shell/sfvm-getbuttoninfo">SFVM_GETBUTTONINFO</a> notification to specify the number of buttons to add to the toolbar, as well as how they're added.

## -struct-fields

### -field cbuttons

Type: <b>UINT</b>

The number of buttons.

### -field uFlags

Type: <b>UINT</b>

One of the following flags.



#### TBIF_APPEND (0)

Add the new buttons after the existing buttons.



#### TBIF_PREPEND (1)

Add the new buttons before the existing buttons.



#### TBIF_REPLACE (2)

Replace the existing buttons with the new buttons.