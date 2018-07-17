---
UID: NS:commctrl.tagDATETIMEPICKERINFO
title: tagDATETIMEPICKERINFO
author: windows-sdk-content
description: Contains information about a date and time picker (DTP) control.
old-location: controls\DATETIMEPICKERINFO.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\datetime\structures\datetimepickerinfo.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: "*LPDATETIMEPICKERINFO, DATETIMEPICKERINFO, DATETIMEPICKERINFO structure [Windows Controls], LPDATETIMEPICKERINFO, LPDATETIMEPICKERINFO structure pointer [Windows Controls], _shell_DATETIMEPICKERINFO, _shell_DATETIMEPICKERINFO_cpp, commctrl/DATETIMEPICKERINFO, commctrl/LPDATETIMEPICKERINFO, controls.DATETIMEPICKERINFO, controls._shell_DATETIMEPICKERINFO, tagDATETIMEPICKERINFO"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DATETIMEPICKERINFO, *LPDATETIMEPICKERINFO
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
req.lib: 
req.dll: 
req.irql: 
---

# tagDATETIMEPICKERINFO structure


## -description


Contains information about a date and time picker (DTP) control.



## -struct-fields




### -field cbSize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Set to <code>sizeof(DATETIMEPICKERINFO)</code>. This member must be set before sending a pointer to this structure with the <a href="https://msdn.microsoft.com/library/Bb761755(v=VS.85).aspx">DTM_GETDATETIMEPICKERINFO</a> message, or the <a href="https://msdn.microsoft.com/library/Bb761786(v=VS.85).aspx">DateTime_GetDateTimePickerInfo</a> macro.


### -field rcCheck

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a></b>

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure describing location of checkbox. If a checkbox is displayed and checked, an edit control should be available to update the selected date-time value.


### -field stateCheck

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

The state of <b>rcCheck</b>—one of the <a href="https://msdn.microsoft.com/1253d2d2-d931-4380-9ae8-f4e1fdaee817">Object State Constants</a>, such as <b>STATE_SYSTEM_CHECKED</b> or <b>STATE_SYSTEM_INVISIBLE</b>.


### -field rcButton

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a></b>

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure describing the location of a drop-down grid or up/down control.


### -field stateButton

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

The state of  <b>rcButton</b>— one or a bitwise combination of the <a href="https://msdn.microsoft.com/1253d2d2-d931-4380-9ae8-f4e1fdaee817">Object State Constants</a>, such as <b>STATE_SYSTEM_UNAVAILABLE</b>, <b>STATE_SYSTEM_INVISIBLE</b>, or <b>STATE_SYSTEM_PRESSED</b>. If the up/down control is in use, the state of the button is  <b>STATE_SYSTEM_INVISIBLE</b>.


### -field hwndEdit

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the edit control. For information see, <a href="https://msdn.microsoft.com/library/Bb775458(v=VS.85).aspx">Edit Controls</a>.


### -field hwndUD

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the up/down control—an alternative to using the drop-down grid (looks like month calendar control). For more information, see <a href="https://msdn.microsoft.com/library/Bb759889(v=VS.85).aspx">Up-Down Controls</a>.


### -field hwndDropDown

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the drop-down grid.

