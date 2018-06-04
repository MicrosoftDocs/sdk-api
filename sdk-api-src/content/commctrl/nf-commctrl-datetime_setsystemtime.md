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

# DateTime_SetSystemtime macro


## -description


Sets a date and time picker (DTP) control to a given date and time. You can use this macro or send the <a href="https://msdn.microsoft.com/aab023ac-22ef-485b-be2f-2aa76dfcf57f">DTM_SETSYSTEMTIME</a> message explicitly. 


## -parameters




### -param hdp

TBD


### -param gd

TBD


### -param pst

TBD






#### - flag

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

A value that specifies the action that should be performed. This should be set to one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GDT_VALID"></a><a id="gdt_valid"></a><dl>
<dt><b>GDT_VALID</b></dt>
</dl>
</td>
<td width="60%">
Set the DTP control according to the data within the <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure pointed to by <i>lpSysTime</i>. 

</td>
</tr>
<tr>
<td width="40%"><a id="GDT_NONE"></a><a id="gdt_none"></a><dl>
<dt><b>GDT_NONE</b></dt>
</dl>
</td>
<td width="60%">
Set the DTP control to "no date" and clear its check box. When this flag is specified, 
						<i>lpSysTime</i> is ignored. This flag applies only to DTP controls that are set to the <a href="Date_and_Time_Picker_Control_Styles.htm">DTS_SHOWNONE</a> style. 

</td>
</tr>
</table>
 


#### - hwndDT

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a DTP control. 


#### - lpSysTime

Type: <b>LPSYSTEMTIME</b>

A pointer to a <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that contains the system time information by which to set the DTP control. 

