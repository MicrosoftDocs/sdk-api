---
UID: NS:commctrl.tagNMDATETIMESTRINGW
title: tagNMDATETIMESTRINGW
author: windows-sdk-content
description: Contains information specific to an edit operation that has taken place in a date and time picker (DTP) control. This message is used with the DTN_USERSTRING notification code.
old-location: controls\NMDATETIMESTRING.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\datetime\structures\nmdatetimestring.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*LPNMDATETIMESTRINGW, LPNMDATETIMESTRING, LPNMDATETIMESTRING structure pointer [Windows Controls], NMDATETIMESTRING, NMDATETIMESTRING structure [Windows Controls], NMDATETIMESTRINGA, NMDATETIMESTRINGW, _win32_NMDATETIMESTRING, _win32_NMDATETIMESTRING_cpp, commctrl/LPNMDATETIMESTRING, commctrl/NMDATETIMESTRING, commctrl/NMDATETIMESTRINGA, commctrl/NMDATETIMESTRINGW, controls.NMDATETIMESTRING, controls._win32_NMDATETIMESTRING, tagNMDATETIMESTRINGW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: NMDATETIMESTRINGW, *LPNMDATETIMESTRINGW
req.redist: 
---

# tagNMDATETIMESTRINGW structure


## -description


Contains information specific to an edit operation that has taken place in a date and time picker (DTP) control. This message is used with the <a href="https://msdn.microsoft.com/en-us/library/Bb761745(v=VS.85).aspx">DTN_USERSTRING</a> notification code. 


## -struct-fields




### -field nmhdr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>

An <a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a> structure that contains information about this notification code. 


### -field pszUserString

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">LPCTSTR</a></b>

The address of the zero-terminated string that the user entered. 


### -field st

Type: <b><a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a></b>

A <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that must be filled in by the owner when handling the <a href="https://msdn.microsoft.com/en-us/library/Bb761745(v=VS.85).aspx">DTN_USERSTRING</a> notification code. 


### -field dwFlags

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">DWORD</a></b>

The return field. Set this member to GDT_VALID to indicate that the 
					<b>st</b> member is valid or to GDT_NONE to set the control to "no date" status (<a href="https://msdn.microsoft.com/en-us/library/Bb761728(v=VS.85).aspx">DTS_SHOWNONE</a> style only). 

