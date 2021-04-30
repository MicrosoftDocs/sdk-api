---
UID: NS:winuser.tagSTYLESTRUCT
title: STYLESTRUCT (winuser.h)
description: Contains the styles for a window.
helpviewer_keywords: ["*LPSTYLESTRUCT","LPSTYLESTRUCT","LPSTYLESTRUCT structure pointer [Windows and Messages]","STYLESTRUCT","STYLESTRUCT structure [Windows and Messages]","_win32_STYLESTRUCT_str","_win32_stylestruct_str_cpp","winmsg.stylestruct","winui._win32_stylestruct_str","winuser/LPSTYLESTRUCT","winuser/STYLESTRUCT"]
old-location: winmsg\stylestruct.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowstructures\stylestruct.htm
ms.date: 12/05/2018
ms.keywords: '*LPSTYLESTRUCT, LPSTYLESTRUCT, LPSTYLESTRUCT structure pointer [Windows and Messages], STYLESTRUCT, STYLESTRUCT structure [Windows and Messages], _win32_STYLESTRUCT_str, _win32_stylestruct_str_cpp, winmsg.stylestruct, winui._win32_stylestruct_str, winuser/LPSTYLESTRUCT, winuser/STYLESTRUCT'
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
req.typenames: STYLESTRUCT, *LPSTYLESTRUCT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagSTYLESTRUCT
 - winuser/tagSTYLESTRUCT
 - LPSTYLESTRUCT
 - winuser/LPSTYLESTRUCT
 - STYLESTRUCT
 - winuser/STYLESTRUCT
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
 - STYLESTRUCT
---

# STYLESTRUCT structure


## -description

Contains the styles for a window.

## -struct-fields

### -field styleOld

Type: <b>DWORD</b>

The previous styles for a window. For more information, see the Remarks.

### -field styleNew

Type: <b>DWORD</b>

The new styles for a window. For more information, see the Remarks.

## -remarks

The styles in 
				<b>styleOld</b> and 
				<b>styleNew</b> can be either the window styles (<b>WS_*</b>) or the extended window styles (<b>WS_EX_*</b>), depending on the 
				<i>wParam</i> of the message that includes <b>STYLESTRUCT</b>.

The 
				<b>styleOld</b> and 
				<b>styleNew</b> members indicate the styles through their bit pattern. Note that several styles are equal to zero; to detect these styles, test for the negation of their inverse style. For example, to see if <b>WS_EX_LEFT</b> is set, you test for ~<b>WS_EX_RIGHT</b>.

## -see-also

<b>Conceptual</b>



<b>Reference</b>



<a href="/windows/desktop/winmsg/wm-stylechanged">WM_STYLECHANGED</a>



<a href="/windows/desktop/winmsg/wm-stylechanging">WM_STYLECHANGING</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>