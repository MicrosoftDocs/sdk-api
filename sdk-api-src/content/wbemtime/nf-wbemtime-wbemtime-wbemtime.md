---
UID: NF:wbemtime.WBEMTime.WBEMTime
title: WBEMTime::WBEMTime (wbemtime.h)
description: The WBEMTime class constructor facilitates conversions between various Windows and ANSI C run-time time formats.
helpviewer_keywords: ["WBEMTime","WBEMTime.WBEMTime","WBEMTime::WBEMTime","WBEMTime::WBEMTime constructors [Windows Management Instrumentation]","wbemtime/WBEMTime::WBEMTime","wmi.wbemtime_wbemtime"]
old-location: wmi\wbemtime_wbemtime.htm
tech.root: wmi
ms.assetid: 8b0ce221-2186-4aed-a474-00f88cef6350
ms.date: 12/05/2018
ms.keywords: WBEMTime, WBEMTime.WBEMTime, WBEMTime::WBEMTime, WBEMTime::WBEMTime constructors [Windows Management Instrumentation], wbemtime/WBEMTime::WBEMTime, wmi.wbemtime_wbemtime
req.header: wbemtime.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WBEMTime::WBEMTime
 - wbemtime/WBEMTime::WBEMTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - WBEMTime::WBEMTime
---

# WBEMTime::WBEMTime


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]
<span>The <b>WBEMTime</b> class constructor facilitates conversions between various Windows and ANSI C run-time time formats.
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Constructor</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr)">WBEMTime()</a>
</td>
<td align="left" width="63%">
Creates an uninitialized time object.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr)">WBEMTime(BSTR)</a>
</td>
<td align="left" width="63%">
Initializes the new time object to the value in the parameter.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttime_t_)">WBEMTime(const time_t&)</a>
</td>
<td align="left" width="63%">
Initializes the new time object to the value in the parameter.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttm_)">WBEMTime(const struct tm)</a>
</td>
<td align="left" width="63%">
Initializes the new time object to the value in the parameter.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constfiletime_)">WBEMTime(const FILETIME&)</a>
</td>
<td align="left" width="63%">
Initializes the new time object to the value in the parameter.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constsystemtime_)">WBEMTime(const SYSTEMTIME&)</a>
</td>
<td align="left" width="63%">
Initializes the new time object to the value in the parameter.

</td>
</tr>
</table>


