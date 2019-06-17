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
f1_keywords: ["wbemtime/WBEMTime"]
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
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>WBEMTime</b> class facilitates conversions between various Windows and ANSI C run-time time formats. For more information, see also <a href="https://docs.microsoft.com/windows/desktop/api/wbemtime/nl-wbemtime-wbemtimespan">WBEMTimeSpan Class Methods</a>.

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
<a href="https://docs.microsoft.com/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr)">WBEMTime</a>
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
<a href="https://docs.microsoft.com/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-clear">Clear</a>
</td>
<td align="left" width="63%">
Sets the time in the <b>WBEMTime</b> object to an invalid time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-getbstr">GetBSTR</a>
</td>
<td align="left" width="63%">
Presents the time as a <b>BSTR</b> value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-getdmtf">GetDMTF</a>
</td>
<td align="left" width="63%">
Gets the time as a <b>BSTR</b> value in CIM datetime format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-getdmtfnonntfs">GetDMTFNonNtfs</a>
</td>
<td align="left" width="63%">
Gets a DMTF date that is based upon a FAT or a <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/date-and-time-format">Date and Time Format</a> where the UTC is not known.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-getfiletime">GetFILETIME</a>
</td>
<td align="left" width="63%">
Gets the time as an MFC <b>FILETIME</b> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa394049(v=vs.85)">GetLocalOffsetForDate</a>
</td>
<td align="left" width="63%">Overloaded. Returns the offset in minutes(+ or -) between GMT and local time for the time supplied in the argument.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-getstructtm">GetStructtm</a>
</td>
<td align="left" width="63%">
Gets the time as an ANSI C run-time <b>struct tm</b> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-getsystemtime">GetSYSTEMTIME</a>
</td>
<td align="left" width="63%">
Gets the time as an MFC <b>SYSTEMTIME</b> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-gettime">GetTime</a>
</td>
<td align="left" width="63%">
Gets the time as a 64-bit integer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-gettime_t">Gettime_t</a>
</td>
<td align="left" width="63%">
Gets the time as an ANSI C run-time time_t variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-isok">IsOk</a>
</td>
<td align="left" width="63%">
Indicates whether the <b>WBEMTime</b> object represents a valid time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-setdmtf">SetDMTF</a>
</td>
<td align="left" width="63%">
Sets the time in the <b>WBEMTime</b> object in CIM datetime format.

</td>
</tr>
</table> 

