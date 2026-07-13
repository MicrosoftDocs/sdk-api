---
UID: NS:commctrl.tagNMDATETIMEFORMATA
title: NMDATETIMEFORMATA (commctrl.h)
description: Contains information about a portion of the format string that defines a callback field within a date and time picker (DTP) control. (ANSI)
helpviewer_keywords: ["*LPNMDATETIMEFORMATA","LPNMDATETIMEFORMAT","LPNMDATETIMEFORMAT structure pointer [Windows Controls]","NMDATETIMEFORMAT","NMDATETIMEFORMAT structure [Windows Controls]","NMDATETIMEFORMATA","NMDATETIMEFORMATW","_win32_NMDATETIMEFORMAT","_win32_NMDATETIMEFORMAT_cpp","commctrl/LPNMDATETIMEFORMAT","commctrl/NMDATETIMEFORMAT","commctrl/NMDATETIMEFORMATA","commctrl/NMDATETIMEFORMATW","controls.NMDATETIMEFORMAT","controls._win32_NMDATETIMEFORMAT"]
old-location: controls\NMDATETIMEFORMAT.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\datetime\structures\nmdatetimeformat.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMDATETIMEFORMATA, LPNMDATETIMEFORMAT, LPNMDATETIMEFORMAT structure pointer [Windows Controls], NMDATETIMEFORMAT, NMDATETIMEFORMAT structure [Windows Controls], NMDATETIMEFORMATA, NMDATETIMEFORMATW, _win32_NMDATETIMEFORMAT, _win32_NMDATETIMEFORMAT_cpp, commctrl/LPNMDATETIMEFORMAT, commctrl/NMDATETIMEFORMAT, commctrl/NMDATETIMEFORMATA, commctrl/NMDATETIMEFORMATW, controls.NMDATETIMEFORMAT, controls._win32_NMDATETIMEFORMAT'
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: NMDATETIMEFORMATW (Unicode) and NMDATETIMEFORMATA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NMDATETIMEFORMATA, *LPNMDATETIMEFORMATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMDATETIMEFORMATA
 - commctrl/tagNMDATETIMEFORMATA
 - LPNMDATETIMEFORMATA
 - commctrl/LPNMDATETIMEFORMATA
 - NMDATETIMEFORMATA
 - commctrl/NMDATETIMEFORMATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - NMDATETIMEFORMAT
 - NMDATETIMEFORMATA
 - NMDATETIMEFORMATW
---

# NMDATETIMEFORMATA structure


## -description

Contains information about a portion of the format string that defines a callback field within a date and time picker (DTP) control. It carries the substring that defines the callback field and contains a buffer to receive the string that will be displayed in the callback field. This structure is used with the <a href="/windows/desktop/Controls/dtn-format">DTN_FORMAT</a> notification code.

## -struct-fields

### -field nmhdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>

An <a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains information about the notification code.

### -field pszFormat

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCTSTR</a></b>

A pointer to the substring that defines a DTP control callback field. The substring consists of one or more "X" characters followed by a NULL character. (For more information about callback fields, see <a href="/windows/desktop/Controls/date-and-time-picker-controls">Callback fields</a>.)

### -field st

Type: <b><a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a></b>

A <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that contains the date and time to be formatted.

### -field pszDisplay

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCTSTR</a></b>

A pointer to a null-terminated string that contains the display text of the control. By default, this is the address of the 
					<b>szDisplay</b> member of this structure. It is acceptable to have <b>pszDisplay</b> point to an existing string. In this case, you do not need to assign a value to <b>szDisplay</b>. However, the string that 
<b>pszDisplay</b> points to must remain valid until another <a href="/windows/desktop/Controls/dtn-format">DTN_FORMAT</a> notification is sent, or until the control is destroyed.

### -field szDisplay

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">TCHAR</a></b>

64-character buffer that is to receive the zero-terminated string that the DTP control will display. It is not necessary to fill the entire buffer.

## -remarks

> [!NOTE]
> The commctrl.h header defines NMDATETIMEFORMAT as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
