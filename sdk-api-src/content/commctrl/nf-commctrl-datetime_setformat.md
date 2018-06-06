---
UID: NF:commctrl.DateTime_SetFormat
title: DateTime_SetFormat macro
author: windows-sdk-content
description: Sets the display of a date and time picker (DTP) control based on a given format string. You can use this macro or send the DTM_SETFORMAT message explicitly.
old-location: controls\DateTime_SetFormat.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\datetime\macros\datetime_setformat.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: DateTime_SetFormat, DateTime_SetFormat macro [Windows Controls], _win32_DateTime_SetFormat, _win32_DateTime_SetFormat_cpp, commctrl/DateTime_SetFormat, controls.DateTime_SetFormat, controls._win32_DateTime_SetFormat
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
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
 - DateTime_SetFormat
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# DateTime_SetFormat macro


## -description


Sets the display of a date and time picker (DTP) control based on a given format string. You can use this macro or send the <a href="https://msdn.microsoft.com/a89fa3ad-9894-4c52-ab56-fb62208e39b3">DTM_SETFORMAT</a> message explicitly. 


## -parameters




### -param hdp

TBD


### -param sz

TBD






#### - hwndDT

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a DTP control. 


#### - lpszFormat

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCTSTR</a></b>

A pointer to a zero-terminated <a href="Date_and_Time_Picker_Controls.htm">format string</a> that defines the desired display. Setting this parameter to <b>NULL</b> will reset the control to the default format string for the current style. 


## -remarks



It is acceptable to include extra characters within the format string to produce a more rich display. However, any nonformat characters must be enclosed within single quotes. For example, the format string "'Today is: 'hh':'m':'s ddddMMMdd', 'yyy" would produce output like "Today is: 04:22:31 Tuesday Mar 23, 1996". 

<div class="alert"><b>Note</b>   A DTP control tracks locale changes when it is using the default format string. If you set a custom format string, it will not be updated in response to locale changes.</div>
<div> </div>


