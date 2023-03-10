---
UID: NF:wbemtime.WBEMTime.GetBSTR
title: WBEMTime::GetBSTR (wbemtime.h)
description: Gets the time as a BSTR value in CIM Date and Time Format.
helpviewer_keywords: ["?GetBSTR@WBEMTime@@QBEPAGXZ","?GetBSTR@WBEMTime@@QEBAPEAGXZ","GetBSTR","GetBSTR method [Windows Management Instrumentation]","GetBSTR method [Windows Management Instrumentation]","WBEMTime interface","WBEMTime interface [Windows Management Instrumentation]","GetBSTR method","WBEMTime.GetBSTR","WBEMTime::GetBSTR","_hmm_wbemtime_getbstr","wbemtime/WBEMTime::GetBSTR","wmi.wbemtime_getbstr"]
old-location: wmi\wbemtime_getbstr.htm
tech.root: wmi
ms.assetid: f1fe92cc-1d51-4bd7-950b-84c76b001163
ms.date: 12/05/2018
ms.keywords: ?GetBSTR@WBEMTime@@QBEPAGXZ, ?GetBSTR@WBEMTime@@QEBAPEAGXZ, GetBSTR, GetBSTR method [Windows Management Instrumentation], GetBSTR method [Windows Management Instrumentation],WBEMTime interface, WBEMTime interface [Windows Management Instrumentation],GetBSTR method, WBEMTime.GetBSTR, WBEMTime::GetBSTR, _hmm_wbemtime_getbstr, wbemtime/WBEMTime::GetBSTR, wmi.wbemtime_getbstr
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
 - WBEMTime::GetBSTR
 - wbemtime/WBEMTime::GetBSTR
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
 - WBEMTime.GetBSTR
 - ?GetBSTR@WBEMTime@@QBEPAGXZ
 - ?GetBSTR@WBEMTime@@QEBAPEAGXZ
---

# WBEMTime::GetBSTR


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetBSTR</b> method gets the time as a <b>BSTR</b> value in 
CIM <a href="/windows/desktop/WmiSdk/date-and-time-format">Date and Time Format</a>.



## -returns

The method returns a <b>BSTR</b> in <a href="/windows/desktop/WmiSdk/date-and-time-format">Date and Time Format</a>. The time is given as GMT. If the internal time value is INVALID_TIME, the method returns <b>NULL</b>.

## -remarks

If the value returned is not <b>NULL</b>, the calling function must call <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> on the returned value. This method returns the same value as <a href="/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-getdmtf">WBEMTime::GetDMTF</a>(false).

## -see-also

<a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a>



<a href="/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-getdmtf">WBEMTime::GetDMTF</a>
