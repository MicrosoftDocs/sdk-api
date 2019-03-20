---
UID: NS:commctrl.tagNMDAYSTATE
title: NMDAYSTATE (commctrl.h)
author: windows-sdk-content
description: Carries information required to process the MCN_GETDAYSTATE notification code. All members of this structure are for input, except prgDayState, which the receiving application must set when processing MCN_GETDAYSTATE.
old-location: controls\NMDAYSTATE.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\monthcal\structures\nmdaystate.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPNMDAYSTATE, LPNMDAYSTATE, LPNMDAYSTATE structure pointer [Windows Controls], NMDAYSTATE, NMDAYSTATE structure [Windows Controls], _win32_NMDAYSTATE, _win32_NMDAYSTATE_cpp, commctrl/LPNMDAYSTATE, commctrl/NMDAYSTATE, controls.NMDAYSTATE, controls._win32_NMDAYSTATE"
ms.topic: struct
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - NMDAYSTATE
product: Windows
targetos: Windows
req.typenames: NMDAYSTATE, *LPNMDAYSTATE
req.redist: 
---

# NMDAYSTATE structure


## -description


Carries information required to process the <a href="https://msdn.microsoft.com/en-us/library/Bb760935(v=VS.85).aspx">MCN_GETDAYSTATE</a> notification code. All members of this structure are for input, except 
			<b>prgDayState</b>, which the receiving application must set when processing MCN_GETDAYSTATE. 


## -struct-fields




### -field nmhdr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>


<a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a> structure that contains information about this notification code. 


### -field stStart

Type: <b><a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a></b>


<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that contains the starting date. 


### -field cDayState

Type: <b>int</b>

INT value specifying the total number of elements that must be in the array at 
					<b>prgDayState</b>. 


### -field prgDayState

Type: <b>LPMONTHDAYSTATE</b>

Address of an array of <a href="https://msdn.microsoft.com/en-us/library/Bb760915(v=VS.85).aspx">MONTHDAYSTATE</a> values. The buffer at this address must be large enough to contain at least 
					<b>cDayState</b> elements. The first element in the array corresponds to the date in 
					<b>stStart</b>. 

