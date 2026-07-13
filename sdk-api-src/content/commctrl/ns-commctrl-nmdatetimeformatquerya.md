---
UID: NS:commctrl.tagNMDATETIMEFORMATQUERYA
title: NMDATETIMEFORMATQUERYA (commctrl.h)
description: Contains information about a date and time picker (DTP) control callback field. (ANSI)
helpviewer_keywords: ["*LPNMDATETIMEFORMATQUERYA","LPNMDATETIMEFORMATQUERY","LPNMDATETIMEFORMATQUERY structure pointer [Windows Controls]","NMDATETIMEFORMATQUERY","NMDATETIMEFORMATQUERY structure [Windows Controls]","NMDATETIMEFORMATQUERYA","NMDATETIMEFORMATQUERYW","_win32_NMDATETIMEFORMATQUERY","_win32_NMDATETIMEFORMATQUERY_cpp","commctrl/LPNMDATETIMEFORMATQUERY","commctrl/NMDATETIMEFORMATQUERY","commctrl/NMDATETIMEFORMATQUERYA","commctrl/NMDATETIMEFORMATQUERYW","controls.NMDATETIMEFORMATQUERY","controls._win32_NMDATETIMEFORMATQUERY"]
old-location: controls\NMDATETIMEFORMATQUERY.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\datetime\structures\nmdatetimeformatquery.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMDATETIMEFORMATQUERYA, LPNMDATETIMEFORMATQUERY, LPNMDATETIMEFORMATQUERY structure pointer [Windows Controls], NMDATETIMEFORMATQUERY, NMDATETIMEFORMATQUERY structure [Windows Controls], NMDATETIMEFORMATQUERYA, NMDATETIMEFORMATQUERYW, _win32_NMDATETIMEFORMATQUERY, _win32_NMDATETIMEFORMATQUERY_cpp, commctrl/LPNMDATETIMEFORMATQUERY, commctrl/NMDATETIMEFORMATQUERY, commctrl/NMDATETIMEFORMATQUERYA, commctrl/NMDATETIMEFORMATQUERYW, controls.NMDATETIMEFORMATQUERY, controls._win32_NMDATETIMEFORMATQUERY'
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: NMDATETIMEFORMATQUERYW (Unicode) and NMDATETIMEFORMATQUERYA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NMDATETIMEFORMATQUERYA, *LPNMDATETIMEFORMATQUERYA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMDATETIMEFORMATQUERYA
 - commctrl/tagNMDATETIMEFORMATQUERYA
 - LPNMDATETIMEFORMATQUERYA
 - commctrl/LPNMDATETIMEFORMATQUERYA
 - NMDATETIMEFORMATQUERYA
 - commctrl/NMDATETIMEFORMATQUERYA
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
 - NMDATETIMEFORMATQUERY
 - NMDATETIMEFORMATQUERYA
 - NMDATETIMEFORMATQUERYW
---

# NMDATETIMEFORMATQUERYA structure


## -description

Contains information about a date and time picker (DTP) control callback field. It contains a substring (taken from the control's format string) that defines a callback field. The structure receives the maximum allowable size of the text that will be displayed in the callback field. This structure is used with the <a href="/windows/desktop/Controls/dtn-formatquery">DTN_FORMATQUERY</a> notification code.

## -struct-fields

### -field nmhdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>

An <a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains information about this notification code.

### -field pszFormat

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCTSTR</a></b>

A pointer to a substring that defines a DTP control callback field. The substring is one or more "X" characters followed by a <b>NULL</b>. (For additional information about callback fields, see <a href="/windows/desktop/Controls/date-and-time-picker-controls">Callback fields</a>.)

### -field szMax

Type: <b><a href="/windows/win32/api/windef/ns-windef-size">SIZE</a></b>

A <a href="/windows/win32/api/windef/ns-windef-size">SIZE</a> structure that must be filled with the maximum size of the text that will be displayed in the callback field.

## -remarks

> [!NOTE]
> The commctrl.h header defines NMDATETIMEFORMATQUERY as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
