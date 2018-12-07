---
UID: NS:commctrl.tagDATETIMEPICKERINFO
title: tagDATETIMEPICKERINFO
author: windows-sdk-content
description: Contains information about a date and time picker (DTP) control.
old-location: controls\DATETIMEPICKERINFO.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\datetime\structures\datetimepickerinfo.htm
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: "*LPDATETIMEPICKERINFO, DATETIMEPICKERINFO, DATETIMEPICKERINFO structure [Windows Controls], LPDATETIMEPICKERINFO, LPDATETIMEPICKERINFO structure pointer [Windows Controls], _shell_DATETIMEPICKERINFO, _shell_DATETIMEPICKERINFO_cpp, commctrl/DATETIMEPICKERINFO, commctrl/LPDATETIMEPICKERINFO, controls.DATETIMEPICKERINFO, controls._shell_DATETIMEPICKERINFO, tagDATETIMEPICKERINFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
 - DATETIMEPICKERINFO
product: Windows
targetos: Windows
req.typenames: DATETIMEPICKERINFO, *LPDATETIMEPICKERINFO
req.redist: 
---

# tagDATETIMEPICKERINFO structure


## -description


Contains information about a date and time picker (DTP) control.



## -struct-fields




### -field cbSize

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">DWORD</a></b>

Set to <code>sizeof(DATETIMEPICKERINFO)</code>. This member must be set before sending a pointer to this structure with the <a href="https://msdn.microsoft.com/en-us/library/Bb761755(v=VS.85).aspx">DTM_GETDATETIMEPICKERINFO</a> message, or the <a href="https://msdn.microsoft.com/en-us/library/Bb761786(v=VS.85).aspx">DateTime_GetDateTimePickerInfo</a> macro.


### -field rcCheck

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a></b>

A <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure describing location of checkbox. If a checkbox is displayed and checked, an edit control should be available to update the selected date-time value.


### -field stateCheck

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">DWORD</a></b>

The state of <b>rcCheck</b>—one of the <a href="https://msdn.microsoft.com/en-us/library/Dd373609(v=VS.85).aspx">Object State Constants</a>, such as <b>STATE_SYSTEM_CHECKED</b> or <b>STATE_SYSTEM_INVISIBLE</b>.


### -field rcButton

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a></b>

A <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure describing the location of a drop-down grid or up/down control.


### -field stateButton

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">DWORD</a></b>

The state of  <b>rcButton</b>— one or a bitwise combination of the <a href="https://msdn.microsoft.com/en-us/library/Dd373609(v=VS.85).aspx">Object State Constants</a>, such as <b>STATE_SYSTEM_UNAVAILABLE</b>, <b>STATE_SYSTEM_INVISIBLE</b>, or <b>STATE_SYSTEM_PRESSED</b>. If the up/down control is in use, the state of the button is  <b>STATE_SYSTEM_INVISIBLE</b>.


### -field hwndEdit

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to the edit control. For information see, <a href="https://msdn.microsoft.com/en-us/library/Bb775458(v=VS.85).aspx">Edit Controls</a>.


### -field hwndUD

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to the up/down control—an alternative to using the drop-down grid (looks like month calendar control). For more information, see <a href="https://msdn.microsoft.com/en-us/library/Bb759889(v=VS.85).aspx">Up-Down Controls</a>.


### -field hwndDropDown

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to the drop-down grid.

