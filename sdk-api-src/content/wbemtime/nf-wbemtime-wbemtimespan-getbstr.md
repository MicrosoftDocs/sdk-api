---
UID: NF:wbemtime.WBEMTimeSpan.GetBSTR
title: WBEMTimeSpan::GetBSTR (wbemtime.h)
description: The GetBSTR method gets the time span as a BSTR in Date and Time format.
helpviewer_keywords: ["GetBSTR","GetBSTR method [Windows Management Instrumentation]","GetBSTR method [Windows Management Instrumentation]","WBEMTimeSpan interface","WBEMTimeSpan interface [Windows Management Instrumentation]","GetBSTR method","WBEMTimeSpan.GetBSTR","WBEMTimeSpan::GetBSTR","_hmm_wbemtimespan_getbstr","wbemtime/WBEMTimeSpan::GetBSTR","wmi.wbemtimespan_getbstr"]
old-location: wmi\wbemtimespan_getbstr.htm
tech.root: wmi
ms.assetid: f5db5a7a-0590-4598-bde7-e90cfc7cd932
ms.date: 12/05/2018
ms.keywords: GetBSTR, GetBSTR method [Windows Management Instrumentation], GetBSTR method [Windows Management Instrumentation],WBEMTimeSpan interface, WBEMTimeSpan interface [Windows Management Instrumentation],GetBSTR method, WBEMTimeSpan.GetBSTR, WBEMTimeSpan::GetBSTR, _hmm_wbemtimespan_getbstr, wbemtime/WBEMTimeSpan::GetBSTR, wmi.wbemtimespan_getbstr
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
 - WBEMTimeSpan::GetBSTR
 - wbemtime/WBEMTimeSpan::GetBSTR
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
 - WBEMTimeSpan.GetBSTR
---

# WBEMTimeSpan::GetBSTR


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/wbemtime/nl-wbemtime-wbemtimespan">WBEMTimeSpan</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetBSTR</b> method gets the time span as a <b>BSTR</b> in <a href="/windows/desktop/WmiSdk/date-and-time-format">Date and Time format</a>.



## -returns

The time span is returned as a <b>BSTR</b> in <a href="/windows/desktop/WmiSdk/date-and-time-format">Date and Time Format</a>.

## -remarks

The calling method must call <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> on the return value.
