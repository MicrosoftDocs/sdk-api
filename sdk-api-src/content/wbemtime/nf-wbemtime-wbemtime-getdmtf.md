---
UID: NF:wbemtime.WBEMTime.GetDMTF
title: WBEMTime::GetDMTF (wbemtime.h)
description: The GetDMTF method converts a BSTR value to CIM Date and Time Format.
helpviewer_keywords: ["?GetDMTF@WBEMTime@@QBEPAGH@Z","?GetDMTF@WBEMTime@@QEBAPEAGH@Z","GetDMTF","GetDMTF method [Windows Management Instrumentation]","GetDMTF method [Windows Management Instrumentation]","WBEMTime interface","WBEMTime interface [Windows Management Instrumentation]","GetDMTF method","WBEMTime.GetDMTF","WBEMTime::GetDMTF","_hmm_wbemtime_getdmtf","wbemtime/WBEMTime::GetDMTF","wmi.wbemtime_getdmtf"]
old-location: wmi\wbemtime_getdmtf.htm
tech.root: wmi
ms.assetid: 3bfcf7f8-0b0c-4a3f-83c7-be4c37753a7a
ms.date: 12/05/2018
ms.keywords: ?GetDMTF@WBEMTime@@QBEPAGH@Z, ?GetDMTF@WBEMTime@@QEBAPEAGH@Z, GetDMTF, GetDMTF method [Windows Management Instrumentation], GetDMTF method [Windows Management Instrumentation],WBEMTime interface, WBEMTime interface [Windows Management Instrumentation],GetDMTF method, WBEMTime.GetDMTF, WBEMTime::GetDMTF, _hmm_wbemtime_getdmtf, wbemtime/WBEMTime::GetDMTF, wmi.wbemtime_getdmtf
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
 - WBEMTime::GetDMTF
 - wbemtime/WBEMTime::GetDMTF
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
 - WBEMTime.GetDMTF
 - ?GetDMTF@WBEMTime@@QBEPAGH@Z
 - ?GetDMTF@WBEMTime@@QEBAPEAGH@Z
---

# WBEMTime::GetDMTF


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetDMTF</b> method converts a  <b>BSTR</b> value to 
CIM <a href="/windows/desktop/WmiSdk/date-and-time-format">Date and Time Format</a>.

## -parameters

### -param bLocal

If <b>TRUE</b>, returns the local time, adjusted for daylight savings time; otherwise, returns GMT.

## -returns

Returns a <b>BSTR</b> in <a href="/windows/desktop/WmiSdk/date-and-time-format">Date and Time Format</a>.

## -remarks

The calling function must call <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> on the return value.

## -see-also

<a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a>



<a href="/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-getbstr">WBEMTime::GetBSTR</a>



<a href="/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-setdmtf">WBEMTime::SetDMTF</a>