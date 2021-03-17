---
UID: NF:wbemtime.WBEMTime.SetDMTF
title: WBEMTime::SetDMTF (wbemtime.h)
description: The SetDMTF method sets the time in the WBEMTime object. The time is given by its BSTR parameter in Date and Time Format. A date and time argument earlier than midnight January 1, 1601 is not valid.
helpviewer_keywords: ["?SetDMTF@WBEMTime@@QAEHQAG@Z","SetDMTF","SetDMTF method [Windows Management Instrumentation]","SetDMTF method [Windows Management Instrumentation]","WBEMTime interface","WBEMTime interface [Windows Management Instrumentation]","SetDMTF method","WBEMTime.SetDMTF","WBEMTime::SetDMTF","_hmm_wbemtime_setdmtf","wbemtime/WBEMTime::SetDMTF","wmi.wbemtime_setdmtf"]
old-location: wmi\wbemtime_setdmtf.htm
tech.root: wmi
ms.assetid: 5a2ed11d-34d8-44b1-a8ce-e8aa7c96c730
ms.date: 12/05/2018
ms.keywords: ?SetDMTF@WBEMTime@@QAEHQAG@Z, SetDMTF, SetDMTF method [Windows Management Instrumentation], SetDMTF method [Windows Management Instrumentation],WBEMTime interface, WBEMTime interface [Windows Management Instrumentation],SetDMTF method, WBEMTime.SetDMTF, WBEMTime::SetDMTF, _hmm_wbemtime_setdmtf, wbemtime/WBEMTime::SetDMTF, wmi.wbemtime_setdmtf
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
 - WBEMTime::SetDMTF
 - wbemtime/WBEMTime::SetDMTF
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - WBEMTime.SetDMTF
 - ?SetDMTF@WBEMTime@@QAEHQAG@Z
---

# WBEMTime::SetDMTF


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>SetDMTF</b> method sets the time in the <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> object. The time is given by its <b>BSTR</b> parameter in Date and Time Format. A date and time argument earlier than midnight January 1, 1601 is not valid.

## -parameters

### -param wszText

<b>BSTR</b> in <a href="/windows/desktop/WmiSdk/date-and-time-format">Date and Time Format</a>.

## -returns

The method returns <b>true</b> if the time is valid and <b>false</b> if the time is not valid.

## -remarks

Internally, <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> stores a datetime as a 64-bit integer. Because of this, implementation-specific interpretation to the use of an asterisk is required when setting a datetime.

When an asterisk "*" appears in any location in the inbound datetime string, <i>wszText</i> is replaced on a positional basis with the default datetime string "16010101000000.000000+000".

The microsecond separator "." and UTC offset sign "+/-" must be present in the correct locations. All other positions are replaced by the default element if an asterisk is detected in the corresponding location.

For example, "1979**********.000000-0*4" becomes "197910101000000.000000-004".

Because <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> internally stores all datetime values in GMT, the resulting UTC of -004 causes the minute field to change so that the internal representation becomes "197910105000000.000000+000".

## -see-also

<a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a>



<a href="/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-getbstr">WBEMTime::GetBSTR</a>



<a href="/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-getdmtf">WBEMTime::GetDMTF</a>