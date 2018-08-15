---
UID: NS:commctrl.tagNMDATETIMEFORMATQUERYW
title: tagNMDATETIMEFORMATQUERYW
author: windows-sdk-content
description: Contains information about a date and time picker (DTP) control callback field.
old-location: controls\NMDATETIMEFORMATQUERY.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\datetime\structures\nmdatetimeformatquery.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPNMDATETIMEFORMATQUERYW, LPNMDATETIMEFORMATQUERY, LPNMDATETIMEFORMATQUERY structure pointer [Windows Controls], NMDATETIMEFORMATQUERY, NMDATETIMEFORMATQUERY structure [Windows Controls], NMDATETIMEFORMATQUERYA, NMDATETIMEFORMATQUERYW, _win32_NMDATETIMEFORMATQUERY, _win32_NMDATETIMEFORMATQUERY_cpp, commctrl/LPNMDATETIMEFORMATQUERY, commctrl/NMDATETIMEFORMATQUERY, commctrl/NMDATETIMEFORMATQUERYA, commctrl/NMDATETIMEFORMATQUERYW, controls.NMDATETIMEFORMATQUERY, controls._win32_NMDATETIMEFORMATQUERY, tagNMDATETIMEFORMATQUERYW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: commctrl.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: NMDATETIMEFORMATQUERYW, *LPNMDATETIMEFORMATQUERYW
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
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# tagNMDATETIMEFORMATQUERYW structure


## -description


Contains information about a date and time picker (DTP) control callback field. It contains a substring (taken from the control's format string) that defines a callback field. The structure receives the maximum allowable size of the text that will be displayed in the callback field. This structure is used with the <a href="https://msdn.microsoft.com/en-us/library/Bb761743(v=VS.85).aspx">DTN_FORMATQUERY</a> notification code. 


## -struct-fields




### -field nmhdr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>

An <a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a> structure that contains information about this notification code. 


### -field pszFormat

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCTSTR</a></b>

A pointer to a substring that defines a DTP control callback field. The substring is one or more "X" characters followed by a <b>NULL</b>. (For additional information about callback fields, see <a href="https://msdn.microsoft.com/en-us/library/Bb761726(v=VS.85).aspx">Callback fields</a>.) 


### -field szMax

Type: <b><a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a></b>

A <a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a> structure that must be filled with the maximum size of the text that will be displayed in the callback field. 

