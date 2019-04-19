---
UID: NL:wbemtime.WBEMTime
title: WBEMTime (wbemtime.h)
author: windows-sdk-content
description: The WBEMTime class facilitates conversions between various Windows and ANSI C run-time time formats. For more information, see also WBEMTimeSpan Class Methods.
old-location: wmi\wbemtime.htm
tech.root: WmiSdk
ms.assetid: b633bc8c-9d02-4bcf-8528-10773fb5ae7a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WBEMTime, WBEMTime class [Windows Management Instrumentation], WBEMTime class [Windows Management Instrumentation],described, _hmm_wbemtime, wbemtime/WBEMTime, wmi.wbemtime
ms.topic: class
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - WBEMTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WBEMTime class


## -description


<p class="CCE_Message">[The <b>WBEMTime</b> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>WBEMTime</b> class facilitates conversions between various Windows and ANSI C run-time time formats. For more information, see also <a href="https://msdn.microsoft.com/bcec87c1-32ba-451b-92bb-80c8a5007adb">WBEMTimeSpan Class Methods</a>.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">WBEMTime</b> has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Constructors</a></li>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul><h3><a id="constructors"></a>Constructors</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">WBEMTime</b> class has these constructors.
<table class="members" id="memberListConstructors">
<tr>
<th align="left" width="37%">Constructor</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b0ce221-2186-4aed-a474-00f88cef6350">WBEMTime</a>
</td>
<td align="left" width="63%">
Constructor that facilitates conversions between various Windows and ANSI C run-time time formats.

</td>
</tr>
</table> 
<h3><a id="methods"></a>Methods</h3>The <b>WBEMTime</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a6b3db6c-1cc8-4058-8d8b-c8126a373130">Clear</a>
</td>
<td align="left" width="63%">
Sets the time in the <b>WBEMTime</b> object to an invalid time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f1fe92cc-1d51-4bd7-950b-84c76b001163">GetBSTR</a>
</td>
<td align="left" width="63%">
Presents the time as a <b>BSTR</b> value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3bfcf7f8-0b0c-4a3f-83c7-be4c37753a7a">GetDMTF</a>
</td>
<td align="left" width="63%">
Gets the time as a <b>BSTR</b> value in CIM datetime format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40353352-da1f-44d8-a2c3-e6fd4639bd98">GetDMTFNonNtfs</a>
</td>
<td align="left" width="63%">
Gets a DMTF date that is based upon a FAT or a <a href="https://msdn.microsoft.com/be239bf8-88a3-47bc-ae4f-49a5195e7a7d">Date and Time Format</a> where the UTC is not known.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3debc121-ff7b-4e2c-9d77-502ee491cad8">GetFILETIME</a>
</td>
<td align="left" width="63%">
Gets the time as an MFC <b>FILETIME</b> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/15cc5f45-604c-4335-bcd3-92d62dc15420">GetLocalOffsetForDate</a>
</td>
<td align="left" width="63%">Overloaded. Returns the offset in minutes(+ or -) between GMT and local time for the time supplied in the argument.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/569e64c5-1b7e-49ef-abaa-be9b2f85269b">GetStructtm</a>
</td>
<td align="left" width="63%">
Gets the time as an ANSI C run-time <b>struct tm</b> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e65cc4e2-36d3-43de-be65-f48ddfb0b273">GetSYSTEMTIME</a>
</td>
<td align="left" width="63%">
Gets the time as an MFC <b>SYSTEMTIME</b> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1690d33d-c39b-448e-889e-48dce1933fc1">GetTime</a>
</td>
<td align="left" width="63%">
Gets the time as a 64-bit integer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62e0faff-4e5a-4bc4-a9a7-a4edbaea9541">Gettime_t</a>
</td>
<td align="left" width="63%">
Gets the time as an ANSI C run-time time_t variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e2d53db3-b247-40ac-9a8f-c6fef9f4e0d3">IsOk</a>
</td>
<td align="left" width="63%">
Indicates whether the <b>WBEMTime</b> object represents a valid time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5a2ed11d-34d8-44b1-a8ce-e8aa7c96c730">SetDMTF</a>
</td>
<td align="left" width="63%">
Sets the time in the <b>WBEMTime</b> object in CIM datetime format.

</td>
</tr>
</table> 

