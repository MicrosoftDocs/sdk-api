---
UID: NF:commctrl.MonthCal_SetCurrentView
title: MonthCal_SetCurrentView macro
author: windows-sdk-content
description: Sets the view for a month calendar control. You can use this macro or send the MCM_SETCURRENTVIEW message explicitly.
old-location: controls\MonthCal_SetCurrentView.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_setcurrentview.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: MCMV_CENTURY, MCMV_DECADE, MCMV_MONTH, MCMV_YEAR, MonthCal_SetCurrentView, MonthCal_SetCurrentView macro [Windows Controls], _shell_MonthCal_SetCurrentView, _shell_MonthCal_SetCurrentView_cpp, commctrl/MonthCal_SetCurrentView, controls.MonthCal_SetCurrentView, controls._shell_MonthCal_SetCurrentView
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: STGOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - MonthCal_SetCurrentView
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# MonthCal_SetCurrentView macro


## -description


Sets the view for a month calendar control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb760998(v=VS.85).aspx">MCM_SETCURRENTVIEW</a> message explicitly.


## -parameters




### -param hmc

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to a month calendar control.


### -param dwNewView

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

New view. One of the following constants.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MCMV_MONTH"></a><a id="mcmv_month"></a><dl>
<dt><b>MCMV_MONTH</b></dt>
</dl>
</td>
<td width="60%">
Monthly view.

</td>
</tr>
<tr>
<td width="40%"><a id="MCMV_YEAR"></a><a id="mcmv_year"></a><dl>
<dt><b>MCMV_YEAR</b></dt>
</dl>
</td>
<td width="60%">
Annual view.

</td>
</tr>
<tr>
<td width="40%"><a id="MCMV_DECADE"></a><a id="mcmv_decade"></a><dl>
<dt><b>MCMV_DECADE</b></dt>
</dl>
</td>
<td width="60%">
Decade view.

</td>
</tr>
<tr>
<td width="40%"><a id="MCMV_CENTURY"></a><a id="mcmv_century"></a><dl>
<dt><b>MCMV_CENTURY</b></dt>
</dl>
</td>
<td width="60%">
Century view.

</td>
</tr>
</table>
 

