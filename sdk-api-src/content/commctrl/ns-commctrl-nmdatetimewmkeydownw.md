---
UID: NS:commctrl.tagNMDATETIMEWMKEYDOWNW
title: NMDATETIMEWMKEYDOWNW (commctrl.h)
description: Carries information used to describe and handle a DTN_WMKEYDOWN notification code.helpviewer_keywords: ["*LPNMDATETIMEWMKEYDOWNW","LPNMDATETIMEWMKEYDOWN","LPNMDATETIMEWMKEYDOWN structure pointer [Windows Controls]","NMDATETIMEWMKEYDOWN","NMDATETIMEWMKEYDOWN structure [Windows Controls]","NMDATETIMEWMKEYDOWNA","NMDATETIMEWMKEYDOWNW","_win32_NMDATETIMEWMKEYDOWN","_win32_NMDATETIMEWMKEYDOWN_cpp","commctrl/LPNMDATETIMEWMKEYDOWN","commctrl/NMDATETIMEWMKEYDOWN","commctrl/NMDATETIMEWMKEYDOWNA","commctrl/NMDATETIMEWMKEYDOWNW","controls.NMDATETIMEWMKEYDOWN","controls._win32_NMDATETIMEWMKEYDOWN"]
old-location: controls\NMDATETIMEWMKEYDOWN.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\datetime\structures\nmdatetimewmkeydown.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMDATETIMEWMKEYDOWNW, LPNMDATETIMEWMKEYDOWN, LPNMDATETIMEWMKEYDOWN structure pointer [Windows Controls], NMDATETIMEWMKEYDOWN, NMDATETIMEWMKEYDOWN structure [Windows Controls], NMDATETIMEWMKEYDOWNA, NMDATETIMEWMKEYDOWNW, _win32_NMDATETIMEWMKEYDOWN, _win32_NMDATETIMEWMKEYDOWN_cpp, commctrl/LPNMDATETIMEWMKEYDOWN, commctrl/NMDATETIMEWMKEYDOWN, commctrl/NMDATETIMEWMKEYDOWNA, commctrl/NMDATETIMEWMKEYDOWNW, controls.NMDATETIMEWMKEYDOWN, controls._win32_NMDATETIMEWMKEYDOWN'
f1_keywords:
- commctrl/NMDATETIMEWMKEYDOWN
dev_langs:
- c++
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: NMDATETIMEWMKEYDOWNW (Unicode) and NMDATETIMEWMKEYDOWNA (ANSI)
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
- Commctrl.h
api_name:
- NMDATETIMEWMKEYDOWN
- NMDATETIMEWMKEYDOWNA
- NMDATETIMEWMKEYDOWNW
targetos: Windows
req.typenames: NMDATETIMEWMKEYDOWNW, *LPNMDATETIMEWMKEYDOWNW
req.redist: 
ms.custom: 19H1
---

# NMDATETIMEWMKEYDOWNW structure


## -description


Carries information used to describe and handle a <a href="https://docs.microsoft.com/windows/desktop/Controls/dtn-wmkeydown">DTN_WMKEYDOWN</a> notification code. 


## -struct-fields




### -field nmhdr

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>

A <a href="https://docs.microsoft.com/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains information about the notification code. 


### -field nVirtKey

Type: <b>int</b>

A virtual key code that represents the key that the user pressed. 


### -field pszFormat

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPCTSTR</a></b>

A zero-terminated substring, taken from the format string, that defines the callback field. The substring is one or more "X" characters, followed by a <b>NULL</b>. 


### -field st

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a></b>

A <a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure containing the current date and time from the DTP control. The owner of the control must modify the time information based on the user's keystroke. 

