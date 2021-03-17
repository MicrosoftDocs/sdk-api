---
UID: NS:commctrl.tagNMDAYSTATE
title: NMDAYSTATE (commctrl.h)
description: Carries information required to process the MCN_GETDAYSTATE notification code. All members of this structure are for input, except prgDayState, which the receiving application must set when processing MCN_GETDAYSTATE.
helpviewer_keywords: ["*LPNMDAYSTATE","LPNMDAYSTATE","LPNMDAYSTATE structure pointer [Windows Controls]","NMDAYSTATE","NMDAYSTATE structure [Windows Controls]","_win32_NMDAYSTATE","_win32_NMDAYSTATE_cpp","commctrl/LPNMDAYSTATE","commctrl/NMDAYSTATE","controls.NMDAYSTATE","controls._win32_NMDAYSTATE"]
old-location: controls\NMDAYSTATE.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\monthcal\structures\nmdaystate.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMDAYSTATE, LPNMDAYSTATE, LPNMDAYSTATE structure pointer [Windows Controls], NMDAYSTATE, NMDAYSTATE structure [Windows Controls], _win32_NMDAYSTATE, _win32_NMDAYSTATE_cpp, commctrl/LPNMDAYSTATE, commctrl/NMDAYSTATE, controls.NMDAYSTATE, controls._win32_NMDAYSTATE'
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
targetos: Windows
req.typenames: NMDAYSTATE, *LPNMDAYSTATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMDAYSTATE
 - commctrl/tagNMDAYSTATE
 - LPNMDAYSTATE
 - commctrl/LPNMDAYSTATE
 - NMDAYSTATE
 - commctrl/NMDAYSTATE
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
 - NMDAYSTATE
---

# NMDAYSTATE structure


## -description

Carries information required to process the <a href="/windows/desktop/Controls/mcn-getdaystate">MCN_GETDAYSTATE</a> notification code. All members of this structure are for input, except 
			<b>prgDayState</b>, which the receiving application must set when processing MCN_GETDAYSTATE.

## -struct-fields

### -field nmhdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>


<a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains information about this notification code.

### -field stStart

Type: <b><a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a></b>


<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that contains the starting date.

### -field cDayState

Type: <b>int</b>

INT value specifying the total number of elements that must be in the array at 
					<b>prgDayState</b>.

### -field prgDayState

Type: <b>LPMONTHDAYSTATE</b>

Address of an array of <a href="/windows/desktop/Controls/monthdaystate">MONTHDAYSTATE</a> values. The buffer at this address must be large enough to contain at least 
					<b>cDayState</b> elements. The first element in the array corresponds to the date in 
					<b>stStart</b>.