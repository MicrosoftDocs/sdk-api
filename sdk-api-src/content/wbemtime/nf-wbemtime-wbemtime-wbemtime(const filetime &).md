---
UID: NF:wbemtime.WBEMTime.WBEMTime(const FILETIME &)
title: WBEMTime::WBEMTime(const FILETIME &)
author: windows-sdk-content
description: The WBEMTime class constructor facilitates conversions between various Windows and ANSI C run-time time formats.
old-location: wmi\wbemtime_wbemtime.htm
old-project: WmiSdk
ms.assetid: 8b0ce221-2186-4aed-a474-00f88cef6350
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: WBEMTime, WBEMTime.WBEMTime, WBEMTime.WBEMTime(const FILETIME &), WBEMTime::WBEMTime, WBEMTime::WBEMTime constructors [Windows Management Instrumentation], WBEMTime::WBEMTime(const FILETIME &), wbemtime/WBEMTime::WBEMTime, wmi.wbemtime_wbemtime
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: WbemTimeout
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
product: Windows
targetos: Windows
req.lib: 
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WBEMTime::WBEMTime(const FILETIME &)


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/b633bc8c-9d02-4bcf-8528-10773fb5ae7a">WBEMTime</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]
<span>The <b>WBEMTime</b> class constructor facilitates conversions between various Windows and ANSI C run-time time formats.
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Constructor</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a0bc9499-594c-4cde-98b5-c0da6c071607">WBEMTime()</a>
</td>
<td align="left" width="63%">
Creates an uninitialized time object.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5a5e6b2-d6f3-4672-b3b1-213d15fb5d13">WBEMTime(BSTR)</a>
</td>
<td align="left" width="63%">
Initializes the new time object to the value in the parameter.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/be698827-c9dc-4f30-9962-2e3f5f2bd029">WBEMTime(const time_t&)</a>
</td>
<td align="left" width="63%">
Initializes the new time object to the value in the parameter.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fe128577-0059-4728-9848-d947697bb386">WBEMTime(const struct tm)</a>
</td>
<td align="left" width="63%">
Initializes the new time object to the value in the parameter.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6538fee8-a807-45ce-abdf-1c20524d78f2">WBEMTime(const FILETIME&)</a>
</td>
<td align="left" width="63%">
Initializes the new time object to the value in the parameter.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02bc92e3-17cd-4102-bbaa-cc3216b426ff">WBEMTime(const SYSTEMTIME&)</a>
</td>
<td align="left" width="63%">
Initializes the new time object to the value in the parameter.

</td>
</tr>
</table>

## -parameters

