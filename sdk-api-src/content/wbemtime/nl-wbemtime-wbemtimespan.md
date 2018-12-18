---
UID: NL:wbemtime.WBEMTimeSpan
title: WBEMTimeSpan
author: windows-sdk-content
description: The WBEMTimeSpan class holds time spans in nanoseconds.
old-location: wmi\wbemtimespan.htm
tech.root: WmiSdk
ms.assetid: bcec87c1-32ba-451b-92bb-80c8a5007adb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WBEMTimeSpan, WBEMTimeSpan class [Windows Management Instrumentation], WBEMTimeSpan class [Windows Management Instrumentation],described, _hmm_wbemtimespan, wbemtime/WBEMTimeSpan, wmi.wbemtimespan
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
 - WBEMTimeSpan
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WBEMTimeSpan class


## -description


<p class="CCE_Message">[The <b>WBEMTimeSpan</b> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>WBEMTimeSpan</b> class holds time spans in nanoseconds.<b>WBEMTimeSpan</b> objects can result from the arithmetic manipulation of <a href="https://msdn.microsoft.com/b633bc8c-9d02-4bcf-8528-10773fb5ae7a">WBEMTime</a> objects. For example, subtracting one <b>WBEMTime</b> object from another results in a <b>WBEMTimeSpan</b> object that represents the difference in time between the two objects. Instances of <b>WBEMTimeSpan</b> can also be used to wrap any data that has an inherent duration, such as the time that remains until a password expires.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">WBEMTimeSpan</b> has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Constructors</a></li>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul><h3><a id="constructors"></a>Constructors</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">WBEMTimeSpan</b> class has these constructors.
<table class="members" id="memberListConstructors">
<tr>
<th align="left" width="37%">Constructor</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa394007(v=VS.85).aspx">WBEMTimeSpan</a>
</td>
<td align="left" width="63%">
Constructor that creates a time span object.

</td>
</tr>
</table> 
<h3><a id="methods"></a>Methods</h3>The <b>WBEMTimeSpan</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa393990(v=VS.85).aspx">Clear</a>
</td>
<td align="left" width="63%">
Sets the time span to INVALID_TIME.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa393997(v=VS.85).aspx">GetBSTR</a>
</td>
<td align="left" width="63%">
Gets the time span as a <b>BSTR</b> in WMI time span format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa393998(v=VS.85).aspx">GetTime</a>
</td>
<td align="left" width="63%">
Returns the time span as a 64-bit integer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa394001(v=VS.85).aspx">IsOk</a>
</td>
<td align="left" width="63%">
Indicates whether the <b>WBEMTimeSpan</b> object represents a valid time span.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b633bc8c-9d02-4bcf-8528-10773fb5ae7a">WBEMTime Class Methods</a>
 

 

