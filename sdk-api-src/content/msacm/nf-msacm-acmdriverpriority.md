---
UID: NF:msacm.acmDriverPriority
title: acmDriverPriority function (msacm.h)
description: The acmDriverPriority function modifies the priority and state of an ACM driver.
helpviewer_keywords: ["_win32_acmDriverPriority","acmDriverPriority","acmDriverPriority function [Windows Multimedia]","msacm/acmDriverPriority","multimedia.acmdriverpriority"]
old-location: multimedia\acmdriverpriority.htm
tech.root: Multimedia
ms.assetid: 62ab009e-b8fe-4b92-ba0f-a98cd761307b
ms.date: 12/05/2018
ms.keywords: _win32_acmDriverPriority, acmDriverPriority, acmDriverPriority function [Windows Multimedia], msacm/acmDriverPriority, multimedia.acmdriverpriority
req.header: msacm.h
req.include-header: 
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
req.lib: Msacm32.lib
req.dll: Msacm32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - acmDriverPriority
 - msacm/acmDriverPriority
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msacm32.dll
 - Ext-MS-Win-mm-msacm-l1-1-0.dll
api_name:
 - acmDriverPriority
---

# acmDriverPriority function


## -description

The <b>acmDriverPriority</b> function modifies the priority and state of an ACM driver.

## -parameters

### -param hadid

Handle to the driver identifier of an installed ACM driver. If the ACM_DRIVERPRIORITYF_BEGIN and ACM_DRIVERPRIORITYF_END flags are specified, this parameter must be <b>NULL</b>.

### -param dwPriority

New priority for a global ACM driver identifier. A zero value specifies that the priority of the driver identifier should remain unchanged. A value of 1 specifies that the driver should be placed as the highest search priority driver. A value of –1 specifies that the driver should be placed as the lowest search priority driver. Priorities are used only for global drivers.

### -param fdwPriority

Flags for setting priorities of ACM drivers. The following values are defined.

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td>ACM_DRIVERPRIORITYF_BEGIN</td>
<td>Change notification broadcasts should be deferred. An application must reenable notification broadcasts as soon as possible with the ACM_DRIVERPRIORITYF_END flag. Note that <i>hadid</i> must be <b>NULL</b>, <i>dwPriority</i> must be zero, and only the ACM_DRIVERPRIORITYF_BEGIN flag can be set.</td>
</tr>
<tr>
<td>ACM_DRIVERPRIORITYF_DISABLE</td>
<td>ACM driver should be disabled if it is currently enabled. Disabling a disabled driver does nothing.</td>
</tr>
<tr>
<td>ACM_DRIVERPRIORITYF_ENABLE</td>
<td>ACM driver should be enabled if it is currently disabled. Enabling an enabled driver does nothing.</td>
</tr>
<tr>
<td>ACM_DRIVERPRIORITYF_END</td>
<td>Calling task wants to reenable change notification broadcasts. An application must call <b>acmDriverPriority</b> with ACM_DRIVERPRIORITYF_END for each successful call with the ACM_DRIVERPRIORITYF_BEGIN flag. Note that <i>hadid</i> must be <b>NULL</b>, <i>dwPriority</i> must be zero, and only the ACM_DRIVERPRIORITYF_END flag can be set.</td>
</tr>
</table>

## -returns

Returns zero if successful or an error otherwise. Possible error values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_ALLOCATED</b></dt>
</dl>
</td>
<td width="60%">
The deferred broadcast lock is owned by a different task.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALFLAG</b></dt>
</dl>
</td>
<td width="60%">
At least one flag is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALHANDLE</b></dt>
</dl>
</td>
<td width="60%">
The specified handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALPARAM</b></dt>
</dl>
</td>
<td width="60%">
At least one parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_NOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The requested operation is not supported for the specified driver. For example, local and notify driver identifiers do not support priorities (but can be enabled and disabled). If an application specifies a nonzero value for <i>dwPriority</i> for local and notify driver identifiers, this error will be returned.

</td>
</tr>
</table>

## -remarks

All driver identifiers can be enabled and disabled, including global, local and notification driver identifiers.

If more than one global driver identifier needs to be enabled, disabled or shifted in priority, an application should defer change notification broadcasts by using the ACM_DRIVERPRIORITYF_BEGIN flag. A single change notification will be broadcast when the ACM_DRIVERPRIORITYF_END flag is specified.

An application can use the function with the <b>acmMetrics</b> ACM_METRIC_DRIVER_PRIORITY metric index to retrieve the current priority of a global driver. Drivers are always enumerated from highest to lowest priority by the <b>acmDriverEnum</b> function.

All enabled driver identifiers will receive change notifications. An application can register a notification message by using the <b>acmDriverAdd</b> function in conjunction with the ACM_DRIVERADDF_NOTIFYHWND flag. Changes to nonglobal driver identifiers will not be broadcast.

Priorities are simply used for the search order when an application does not specify a driver. Boosting the priority of a driver will have no effect on the performance of a driver.

## -see-also

<a href="/windows/desktop/Multimedia/audio-compression-functions">Audio Compression Functions</a>



<a href="/windows/desktop/Multimedia/audio-compression-manager">Audio Compression Manager</a>