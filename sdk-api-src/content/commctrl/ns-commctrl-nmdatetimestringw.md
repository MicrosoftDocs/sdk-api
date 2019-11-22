---
UID: NS:commctrl.tagNMDATETIMESTRINGW
title: NMDATETIMESTRINGW (commctrl.h)

description: Contains information specific to an edit operation that has taken place in a date and time picker (DTP) control. This message is used with the DTN_USERSTRING notification code.
old-location: controls\NMDATETIMESTRING.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\datetime\structures\nmdatetimestring.htm

ms.date: 12/05/2018
ms.keywords: '*LPNMDATETIMESTRINGW, LPNMDATETIMESTRING, LPNMDATETIMESTRING structure pointer [Windows Controls], NMDATETIMESTRING, NMDATETIMESTRING structure [Windows Controls], NMDATETIMESTRINGA, NMDATETIMESTRINGW, _win32_NMDATETIMESTRING, _win32_NMDATETIMESTRING_cpp, commctrl/LPNMDATETIMESTRING, commctrl/NMDATETIMESTRING, commctrl/NMDATETIMESTRINGA, commctrl/NMDATETIMESTRINGW, controls.NMDATETIMESTRING, controls._win32_NMDATETIMESTRING'
ms.topic: struct
f1_keywords:
- commctrl/NMDATETIMESTRING
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
req.unicode-ansi: NMDATETIMESTRINGW (Unicode) and NMDATETIMESTRINGA (ANSI)
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
- NMDATETIMESTRING
- NMDATETIMESTRINGA
- NMDATETIMESTRINGW
targetos: Windows
req.typenames: NMDATETIMESTRINGW, *LPNMDATETIMESTRINGW
req.redist: 
ms.custom: 19H1
---

# NMDATETIMESTRINGW structure


## -description


Contains information specific to an edit operation that has taken place in a date and time picker (DTP) control. This message is used with the <a href="https://docs.microsoft.com/windows/desktop/Controls/dtn-userstring">DTN_USERSTRING</a> notification code. 


## -struct-fields




### -field nmhdr

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>

An <a href="https://docs.microsoft.com/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains information about this notification code. 


### -field pszUserString

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPCTSTR</a></b>

The address of the zero-terminated string that the user entered. 


### -field st

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a></b>

A <a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that must be filled in by the owner when handling the <a href="https://docs.microsoft.com/windows/desktop/Controls/dtn-userstring">DTN_USERSTRING</a> notification code. 


### -field dwFlags

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

The return field. Set this member to GDT_VALID to indicate that the 
					<b>st</b> member is valid or to GDT_NONE to set the control to "no date" status (<a href="https://docs.microsoft.com/windows/desktop/Controls/date-and-time-picker-control-styles">DTS_SHOWNONE</a> style only). 

