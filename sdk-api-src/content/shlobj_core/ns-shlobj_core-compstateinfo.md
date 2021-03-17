---
UID: NS:shlobj_core._tagCOMPSTATEINFO
title: COMPSTATEINFO (shlobj_core.h)
description: Used by Windows 2000 to hold information about a component's state.
helpviewer_keywords: ["*LPCOMPSTATEINFO","COMPSTATEINFO","COMPSTATEINFO structure [Windows Shell]","IS_FULLSCREEN","IS_NORMAL","IS_SPLIT","LPCOMPSTATEINFO","LPCOMPSTATEINFO structure pointer [Windows Shell]","_tagCOMPSTATEINFO","_win32_COMPSTATEINFO","shell.COMPSTATEINFO","shlobj_core/COMPSTATEINFO","shlobj_core/LPCOMPSTATEINFO"]
old-location: shell\COMPSTATEINFO.htm
tech.root: shell
ms.assetid: 0087e868-0bdd-4ad2-a93f-84ff55b2cb06
ms.date: 12/05/2018
ms.keywords: '*LPCOMPSTATEINFO, COMPSTATEINFO, COMPSTATEINFO structure [Windows Shell], IS_FULLSCREEN, IS_NORMAL, IS_SPLIT, LPCOMPSTATEINFO, LPCOMPSTATEINFO structure pointer [Windows Shell], _tagCOMPSTATEINFO, _win32_COMPSTATEINFO, shell.COMPSTATEINFO, shlobj_core/COMPSTATEINFO, shlobj_core/LPCOMPSTATEINFO'
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: COMPSTATEINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _tagCOMPSTATEINFO
 - shlobj_core/_tagCOMPSTATEINFO
 - COMPSTATEINFO
 - shlobj_core/COMPSTATEINFO
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
 - COMPSTATEINFO
---

# COMPSTATEINFO structure


## -description

Used by Windows 2000 to hold information about a component's state.

## -struct-fields

### -field dwSize

Type: <b>DWORD</b>

The size of the structure.

### -field iLeft

Type: <b>int</b>

The left edge of the top-left corner in screen coordinates.

### -field iTop

Type: <b>int</b>

The top of the top-left corner in screen coordinates.

### -field dwWidth

Type: <b>DWORD</b>

The width, in pixels.

### -field dwHeight

Type: <b>DWORD</b>

The height, in pixels.

### -field dwItemState

Type: <b>DWORD</b>

The state of the component.



#### IS_NORMAL

Normal screen.



#### IS_FULLSCREEN

Full screen.



#### IS_SPLIT

Split screen.

