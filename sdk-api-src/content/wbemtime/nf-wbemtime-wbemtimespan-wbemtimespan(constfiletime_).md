---
UID: NF:wbemtime.WBEMTimeSpan.WBEMTimeSpan(constFILETIME&)
title: WBEMTimeSpan::WBEMTimeSpan(const FILETIME &) (wbemtime.h)
description: The WBEMTimeSpan class constructor creates a time span object. The constructor is overloaded. (overload 1/3)
helpviewer_keywords: ["WBEMTimeSpan","WBEMTimeSpan.WBEMTimeSpan","WBEMTimeSpan.WBEMTimeSpan(const FILETIME &)","WBEMTimeSpan::WBEMTimeSpan","WBEMTimeSpan::WBEMTimeSpan constructors [Windows Management Instrumentation]","WBEMTimeSpan::WBEMTimeSpan(const FILETIME &)","WBEMTimeSpan::WbemTimeSpan","wbemtime/WBEMTimeSpan::WBEMTimeSpan","wmi.wbemtimespan_wbemtimespan"]
old-location: wmi\wbemtimespan_wbemtimespan.htm
tech.root: wmi
ms.assetid: 337dc247-9904-457a-a1f3-e1cf29b61126
ms.date: 12/05/2018
ms.keywords: WBEMTimeSpan, WBEMTimeSpan.WBEMTimeSpan, WBEMTimeSpan.WBEMTimeSpan(const FILETIME &), WBEMTimeSpan::WBEMTimeSpan, WBEMTimeSpan::WBEMTimeSpan constructors [Windows Management Instrumentation], WBEMTimeSpan::WBEMTimeSpan(const FILETIME &), WBEMTimeSpan::WbemTimeSpan, wbemtime/WBEMTimeSpan::WBEMTimeSpan, wmi.wbemtimespan_wbemtimespan
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
 - WBEMTimeSpan::WBEMTimeSpan
 - wbemtime/WBEMTimeSpan::WBEMTimeSpan
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
 - WBEMTimeSpan::WbemTimeSpan
---

# WBEMTimeSpan::WBEMTimeSpan(const FILETIME &)


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/wbemtime/nl-wbemtime-wbemtimespan">WBEMTimeSpan</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]
<span>The <b>WBEMTimeSpan</b> class constructor creates a 
    time span object. The constructor is overloaded.
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Constructor</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr)">WBEMTimeSpan()</a>
</td>
<td align="left" width="63%">
Creates an uninitialized time span object.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr)">WBEMTimeSpan(BSTR)</a>
</td>
<td align="left" width="63%">
Initializes the new time span object to value in the parameter.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(int_int_int_int_int_int_int)">WBEMTimeSpan(int,int,int,int,int,int,int)</a>
</td>
<td align="left" width="63%">
Initializes the new time span object to values in the parameters.

</td>
</tr>
</table>

## -parameters
