---
UID: NF:mmiscapi.DriverCallback
title: DriverCallback function (mmiscapi.h)
description: Calls a callback function, sends a message to a window, or unblocks a thread. The action depends on the value of the notification flag. This function is intended to be used only within the DriverProc function of an installable driver.
helpviewer_keywords: ["DCB_FUNCTION","DCB_NOSWITCH","DCB_TASK","DCB_WINDOW","DriverCallback","DriverCallback function [Windows Multimedia]","_win32_DriverCallback","digitalv/DriverCallback","multimedia.drivercallback"]
old-location: multimedia\drivercallback.htm
tech.root: Multimedia
ms.assetid: 89afeb47-0a98-4db1-8664-6a0fe66d3413
ms.date: 12/05/2018
ms.keywords: DCB_FUNCTION, DCB_NOSWITCH, DCB_TASK, DCB_WINDOW, DriverCallback, DriverCallback function [Windows Multimedia], _win32_DriverCallback, digitalv/DriverCallback, multimedia.drivercallback
req.header: mmiscapi.h
req.include-header: Mmiscapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winmm.lib
req.dll: Winmm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DriverCallback
 - mmiscapi/DriverCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winmm.dll
 - API-MS-Win-mm-misc-l1-1-0.dll
 - winmmbase.dll
 - API-MS-Win-mm-misc-l1-1-1.dll
api_name:
 - DriverCallback
---

# DriverCallback function


## -description

Calls a callback function, sends a message to a window, or unblocks a thread. The action depends on the value of the notification flag. This function is intended to be used only within the <a href="/previous-versions/dd797918(v=vs.85)">DriverProc</a> function of an installable driver.

## -parameters

### -param dwCallback

Address of the callback function, a window handle, or a task handle, depending on the flag specified in the <i>dwFlags</i> parameter.

### -param dwFlags

Notification flags. It can be one of these values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DCB_NOSWITCH"></a><a id="dcb_noswitch"></a><dl>
<dt><b>DCB_NOSWITCH</b></dt>
</dl>
</td>
<td width="60%">
The system is prevented from switching stacks. This value is only used if enough stack space for the callback function is known to exist.

</td>
</tr>
<tr>
<td width="40%"><a id="DCB_FUNCTION"></a><a id="dcb_function"></a><dl>
<dt><b>DCB_FUNCTION</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwCallback</i> parameter is the address of an application-defined callback function. The system sends the callback message to the callback function.

</td>
</tr>
<tr>
<td width="40%"><a id="DCB_WINDOW"></a><a id="dcb_window"></a><dl>
<dt><b>DCB_WINDOW</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwCallback</i> parameter is the handle of an application-defined window. The system sends subsequent notifications to the window.

</td>
</tr>
<tr>
<td width="40%"><a id="DCB_TASK"></a><a id="dcb_task"></a><dl>
<dt><b>DCB_TASK</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwCallback</i> parameter is the handle of an application or task. The system sends subsequent notifications to the application or task.

</td>
</tr>
</table>

### -param hDevice

Handle of the installable driver instance.

### -param dwMsg

Message value.

### -param dwUser

32-bit user-instance data supplied by the application when the device was opened.

### -param dwParam1

32-bit message-dependent parameter.

### -param dwParam2

32-bit message-dependent parameter.

## -returns

Returns <b>TRUE</b> if successful or <b>FALSE</b> if a parameter is invalid or the task's message queue is full.

## -remarks

The client specifies how to notify it when the device is opened. The DCB_FUNCTION and DCB_WINDOW flags are equivalent to the high-order word of the corresponding flags CALLBACK_FUNCTION and CALLBACK_WINDOW specified in the <i>lParam2</i> parameter of the <a href="/windows/desktop/Multimedia/drv-open">DRV_OPEN</a> message when the device was opened.

If notification is accomplished with a callback function, <i>hdrvr</i>, <i>msg</i>, <i>dwUser</i>, <i>dwParam1</i>, and <i>dwParam2</i> are passed to the callback function. If notification is accomplished by means of a window, only <i>msg</i>, <i>hdrvr</i>, and <i>dwParam1</i> are passed to the window.

## -see-also

<a href="/windows/desktop/Multimedia/driver-functions">Driver Functions</a>



<a href="/windows/desktop/Multimedia/installable-drivers">Installable Drivers</a>