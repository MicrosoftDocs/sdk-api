---
UID: NS:winuser.tagMOUSEMOVEPOINT
title: MOUSEMOVEPOINT (winuser.h)
description: Contains information about the mouse's location in screen coordinates.
helpviewer_keywords: ["*LPMOUSEMOVEPOINT","*PMOUSEMOVEPOINT","MOUSEMOVEPOINT","MOUSEMOVEPOINT structure [Keyboard and Mouse Input]","PMOUSEMOVEPOINT","PMOUSEMOVEPOINT structure pointer [Keyboard and Mouse Input]","_win32_MOUSEMOVEPOINT_str","_win32_mousemovepoint_str_cpp","inputdev.mousemovepoint","winui._win32_mousemovepoint_str","winuser/MOUSEMOVEPOINT","winuser/PMOUSEMOVEPOINT"]
old-location: inputdev\mousemovepoint.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\mouseinput\mouseinputreference\mouseinputstructures\mousemovepoint.htm
ms.date: 12/05/2018
ms.keywords: '*LPMOUSEMOVEPOINT, *PMOUSEMOVEPOINT, MOUSEMOVEPOINT, MOUSEMOVEPOINT structure [Keyboard and Mouse Input], PMOUSEMOVEPOINT, PMOUSEMOVEPOINT structure pointer [Keyboard and Mouse Input], _win32_MOUSEMOVEPOINT_str, _win32_mousemovepoint_str_cpp, inputdev.mousemovepoint, winui._win32_mousemovepoint_str, winuser/MOUSEMOVEPOINT, winuser/PMOUSEMOVEPOINT'
req.header: winuser.h
req.include-header: Windows.h
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
req.typenames: MOUSEMOVEPOINT, *PMOUSEMOVEPOINT, *LPMOUSEMOVEPOINT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMOUSEMOVEPOINT
 - winuser/tagMOUSEMOVEPOINT
 - PMOUSEMOVEPOINT
 - winuser/PMOUSEMOVEPOINT
 - MOUSEMOVEPOINT
 - winuser/MOUSEMOVEPOINT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - MOUSEMOVEPOINT
---

# MOUSEMOVEPOINT structure


## -description

Contains information about the mouse's location in screen coordinates.

## -struct-fields

### -field x

Type: <b>int</b>

The x-coordinate of the mouse.

### -field y

Type: <b>int</b>

The y-coordinate of the mouse.

### -field time

Type: <b>DWORD</b>

The time stamp of the mouse coordinate.

### -field dwExtraInfo

Type: <b>ULONG_PTR</b>

Additional information associated with this coordinate.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getmousemovepointsex">GetMouseMovePointsEx</a>



<a href="/windows/desktop/inputdev/mouse-input">Mouse Input</a>



<b>Reference</b>