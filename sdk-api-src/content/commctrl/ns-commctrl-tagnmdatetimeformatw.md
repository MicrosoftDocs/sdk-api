---
UID: NS:commctrl.tagNMDATETIMEFORMATW
title: tagNMDATETIMEFORMATW
author: windows-sdk-content
description: Contains information about a portion of the format string that defines a callback field within a date and time picker (DTP) control.
old-location: controls\NMDATETIMEFORMAT.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\datetime\structures\nmdatetimeformat.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*LPNMDATETIMEFORMATW, LPNMDATETIMEFORMAT, LPNMDATETIMEFORMAT structure pointer [Windows Controls], NMDATETIMEFORMAT, NMDATETIMEFORMAT structure [Windows Controls], NMDATETIMEFORMATA, NMDATETIMEFORMATW, _win32_NMDATETIMEFORMAT, _win32_NMDATETIMEFORMAT_cpp, commctrl/LPNMDATETIMEFORMAT, commctrl/NMDATETIMEFORMAT, commctrl/NMDATETIMEFORMATA, commctrl/NMDATETIMEFORMATW, controls.NMDATETIMEFORMAT, controls._win32_NMDATETIMEFORMAT, tagNMDATETIMEFORMATW"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: NMDATETIMEFORMATW, *LPNMDATETIMEFORMATW
req.redist: 
---

# tagNMDATETIMEFORMATW structure


## -description


Contains information about a portion of the format string that defines a callback field within a date and time picker (DTP) control. It carries the substring that defines the callback field and contains a buffer to receive the string that will be displayed in the callback field. This structure is used with the <a href="https://msdn.microsoft.com/en-us/library/Bb761741(v=VS.85).aspx">DTN_FORMAT</a> notification code. 


## -struct-fields




### -field nmhdr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>

An <a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a> structure that contains information about the notification code. 


### -field pszFormat

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">LPCTSTR</a></b>

A pointer to the substring that defines a DTP control callback field. The substring consists of one or more "X" characters followed by a NULL character. (For more information about callback fields, see <a href="https://msdn.microsoft.com/en-us/library/Bb761726(v=VS.85).aspx">Callback fields</a>.) 


### -field st

Type: <b><a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a></b>

A <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that contains the date and time to be formatted. 


### -field pszDisplay

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">LPCTSTR</a></b>

A pointer to a null-terminated string that contains the display text of the control. By default, this is the address of the 
					<b>szDisplay</b> member of this structure. It is acceptable to have <b>pszDisplay</b> point to an existing string. In this case, you do not need to assign a value to <b>szDisplay</b>. However, the string that 
<b>pszDisplay</b> points to must remain valid until another <a href="https://msdn.microsoft.com/en-us/library/Bb761741(v=VS.85).aspx">DTN_FORMAT</a> notification is sent, or until the control is destroyed. 


### -field szDisplay

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">TCHAR</a></b>

64-character buffer that is to receive the zero-terminated string that the DTP control will display. It is not necessary to fill the entire buffer. 

