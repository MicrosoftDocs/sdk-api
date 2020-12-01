---
UID: NF:wbemtime.WBEMTime.WBEMTime(constBSTR)
title: WBEMTime::WBEMTime(const BSTR) (wbemtime.h)
description: The WBEMTime class constructor overload method takes a BSTR parameter.
helpviewer_keywords: ["??0WBEMTime@@QAE@QAG@Z","??0WBEMTime@@QEAA@QEAG@Z","WBEMTime","WBEMTime constructor [Windows Management Instrumentation]","WBEMTime constructor [Windows Management Instrumentation]","WBEMTime interface","WBEMTime interface [Windows Management Instrumentation]","WBEMTime constructor","WBEMTime.WBEMTime","WBEMTime.WBEMTime(const BSTR)","WBEMTime::WBEMTime","WBEMTime::WBEMTime(BSTR)","WBEMTime::WBEMTime(const BSTR)","wbemtime/WBEMTime::WBEMTime","wmi.wbemtime_wbemtime_bstr_"]
old-location: wmi\wbemtime_wbemtime_bstr_.htm
tech.root: wmi
ms.assetid: a5a5e6b2-d6f3-4672-b3b1-213d15fb5d13
ms.date: 12/05/2018
ms.keywords: ??0WBEMTime@@QAE@QAG@Z, ??0WBEMTime@@QEAA@QEAG@Z, WBEMTime, WBEMTime constructor [Windows Management Instrumentation], WBEMTime constructor [Windows Management Instrumentation],WBEMTime interface, WBEMTime interface [Windows Management Instrumentation],WBEMTime constructor, WBEMTime.WBEMTime, WBEMTime.WBEMTime(const BSTR), WBEMTime::WBEMTime, WBEMTime::WBEMTime(BSTR), WBEMTime::WBEMTime(const BSTR), wbemtime/WBEMTime::WBEMTime, wmi.wbemtime_wbemtime_bstr_
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
 - WBEMTime.WBEMTime
 - ??0WBEMTime@@QAE@QAG@Z
 - ??0WBEMTime@@QEAA@QEAG@Z
---

# WBEMTime::WBEMTime(const BSTR)


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> class constructor overload method takes a <b>BSTR</b> parameter.

## -parameters

### -param bstrDMTFFormat

<b>BSTR</b> in Date and Time Format. The <b>BSTR</b> is converted to GMT.

Now when you use <a href="/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-getdmtf">WBEMTime::GetDMTF</a> to retrieve it you have only two choices:

<ul>
<li>Get as Local Time</li>
<li>Get as GMT</li>
</ul>
At this point, the actual offset used in the <b>BSTR</b> to build the <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> object has been lost.

## -remarks

If you use the <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a>( <b>BSTR</b> <i>bstrDMTFFormat</i>) form of the constructor, you can only retrieve the time in one of these ways:

<ul>
<li>Get as Local Time</li>
<li>Get as GMT</li>
</ul>
The actual offset used in the <b>BSTR</b> to build the <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> object has been lost.

Should an "*" appear in any location in the inbound datetime string <i>bstrDMTFFormat</i>, the * is replaced on a positional basis with the default datetime string "16010101000000.000000+000".

The microsecond separator "." and UTC offset sign "+/-" must be present in the correct locations. "* "in these locations constitutes an error. All other positions are replaced by the default element if "*" is detected in the corresponding location. Invalid character symbols are not allowed.

Example: "1979**********.000000+000"  appears as "197910101000000.000000+000".

"1979**********.000000+0*1" converts to "197910101000000.000000+001". Note the "*" in the UTC offset changes to 0 in the second position. On reading this datetime field the resulting UTC of 001 impacts the minute field to yield "197910100000000.000000+000".