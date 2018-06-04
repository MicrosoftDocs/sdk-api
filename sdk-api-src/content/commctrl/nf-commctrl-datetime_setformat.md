---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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


