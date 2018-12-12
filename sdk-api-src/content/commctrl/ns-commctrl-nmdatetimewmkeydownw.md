---
UID: NS:commctrl.tagNMDATETIMEWMKEYDOWNW
title: NMDATETIMEWMKEYDOWNW
author: windows-sdk-content
description: Carries information used to describe and handle a DTN_WMKEYDOWN notification code.
old-location: controls\NMDATETIMEWMKEYDOWN.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\datetime\structures\nmdatetimewmkeydown.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPNMDATETIMEWMKEYDOWNW, LPNMDATETIMEWMKEYDOWN, LPNMDATETIMEWMKEYDOWN structure pointer [Windows Controls], NMDATETIMEWMKEYDOWN, NMDATETIMEWMKEYDOWN structure [Windows Controls], NMDATETIMEWMKEYDOWNA, NMDATETIMEWMKEYDOWNW, _win32_NMDATETIMEWMKEYDOWN, _win32_NMDATETIMEWMKEYDOWN_cpp, commctrl/LPNMDATETIMEWMKEYDOWN, commctrl/NMDATETIMEWMKEYDOWN, commctrl/NMDATETIMEWMKEYDOWNA, commctrl/NMDATETIMEWMKEYDOWNW, controls.NMDATETIMEWMKEYDOWN, controls._win32_NMDATETIMEWMKEYDOWN"
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
product: Windows
targetos: Windows
req.typenames: NMDATETIMEWMKEYDOWNW, *LPNMDATETIMEWMKEYDOWNW
req.redist: 
---

# NMDATETIMEWMKEYDOWNW structure


## -description


Carries information used to describe and handle a <a href="https://msdn.microsoft.com/e67e222d-28a1-4d30-ae64-8ec9a62fa321">DTN_WMKEYDOWN</a> notification code. 


## -struct-fields




### -field nmhdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>

A <a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that contains information about the notification code. 


### -field nVirtKey

Type: <b>int</b>

A virtual key code that represents the key that the user pressed. 


### -field pszFormat

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCTSTR</a></b>

A zero-terminated substring, taken from the format string, that defines the callback field. The substring is one or more "X" characters, followed by a <b>NULL</b>. 


### -field st

Type: <b><a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a></b>

A <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure containing the current date and time from the DTP control. The owner of the control must modify the time information based on the user's keystroke. 

