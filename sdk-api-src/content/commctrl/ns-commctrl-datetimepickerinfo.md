---
UID: NS:commctrl.tagDATETIMEPICKERINFO
title: DATETIMEPICKERINFO (commctrl.h)
description: Contains information about a date and time picker (DTP) control.
helpviewer_keywords: ["*LPDATETIMEPICKERINFO","DATETIMEPICKERINFO","DATETIMEPICKERINFO structure [Windows Controls]","LPDATETIMEPICKERINFO","LPDATETIMEPICKERINFO structure pointer [Windows Controls]","_shell_DATETIMEPICKERINFO","_shell_DATETIMEPICKERINFO_cpp","commctrl/DATETIMEPICKERINFO","commctrl/LPDATETIMEPICKERINFO","controls.DATETIMEPICKERINFO","controls._shell_DATETIMEPICKERINFO"]
old-location: controls\DATETIMEPICKERINFO.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\datetime\structures\datetimepickerinfo.htm
ms.date: 12/05/2018
ms.keywords: '*LPDATETIMEPICKERINFO, DATETIMEPICKERINFO, DATETIMEPICKERINFO structure [Windows Controls], LPDATETIMEPICKERINFO, LPDATETIMEPICKERINFO structure pointer [Windows Controls], _shell_DATETIMEPICKERINFO, _shell_DATETIMEPICKERINFO_cpp, commctrl/DATETIMEPICKERINFO, commctrl/LPDATETIMEPICKERINFO, controls.DATETIMEPICKERINFO, controls._shell_DATETIMEPICKERINFO'
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
targetos: Windows
req.typenames: DATETIMEPICKERINFO, *LPDATETIMEPICKERINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDATETIMEPICKERINFO
 - commctrl/tagDATETIMEPICKERINFO
 - LPDATETIMEPICKERINFO
 - commctrl/LPDATETIMEPICKERINFO
 - DATETIMEPICKERINFO
 - commctrl/DATETIMEPICKERINFO
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
 - DATETIMEPICKERINFO
---

# DATETIMEPICKERINFO structure


## -description

Contains information about a date and time picker (DTP) control.

## -struct-fields

### -field cbSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Set to <code>sizeof(DATETIMEPICKERINFO)</code>. This member must be set before sending a pointer to this structure with the <a href="/windows/desktop/Controls/dtm-getdatetimepickerinfo">DTM_GETDATETIMEPICKERINFO</a> message, or the <a href="/windows/desktop/api/commctrl/nf-commctrl-datetime_getdatetimepickerinfo">DateTime_GetDateTimePickerInfo</a> macro.

### -field rcCheck

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>

A <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure describing location of checkbox. If a checkbox is displayed and checked, an edit control should be available to update the selected date-time value.

### -field stateCheck

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

The state of <b>rcCheck</b>—one of the <a href="/windows/desktop/WinAuto/object-state-constants">Object State Constants</a>, such as <b>STATE_SYSTEM_CHECKED</b> or <b>STATE_SYSTEM_INVISIBLE</b>.

### -field rcButton

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>

A <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure describing the location of a drop-down grid or up/down control.

### -field stateButton

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

The state of  <b>rcButton</b>— one or a bitwise combination of the <a href="/windows/desktop/WinAuto/object-state-constants">Object State Constants</a>, such as <b>STATE_SYSTEM_UNAVAILABLE</b>, <b>STATE_SYSTEM_INVISIBLE</b>, or <b>STATE_SYSTEM_PRESSED</b>. If the up/down control is in use, the state of the button is  <b>STATE_SYSTEM_INVISIBLE</b>.

### -field hwndEdit

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the edit control. For information see, <a href="/windows/desktop/Controls/edit-controls">Edit Controls</a>.

### -field hwndUD

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the up/down control—an alternative to using the drop-down grid (looks like month calendar control). For more information, see <a href="/windows/desktop/Controls/up-down-controls">Up-Down Controls</a>.

### -field hwndDropDown

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the drop-down grid.