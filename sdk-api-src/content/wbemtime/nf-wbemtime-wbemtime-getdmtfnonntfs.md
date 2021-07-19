---
UID: NF:wbemtime.WBEMTime.GetDMTFNonNtfs
title: WBEMTime::GetDMTFNonNtfs (wbemtime.h)
description: The GetDMTFNonNtfs method gets a DMTF date in a CIM Date and Time Format from a FAT that does not have time zones.
helpviewer_keywords: ["?GetDMTFNonNtfs@WBEMTime@@QBEPAGXZ","?GetDMTFNonNtfs@WBEMTime@@QEBAPEAGXZ","GetDMTFNonNtfs","GetDMTFNonNtfs method [Windows Management Instrumentation]","GetDMTFNonNtfs method [Windows Management Instrumentation]","WBEMTime interface","WBEMTime interface [Windows Management Instrumentation]","GetDMTFNonNtfs method","WBEMTime.GetDMTFNonNtfs","WBEMTime::GetDMTFNonNtfs","_hmm_wbemtime_getdmtfnonntfs","wbemtime/WBEMTime::GetDMTFNonNtfs","wmi.wbemtime_getdmtfnonntfs"]
old-location: wmi\wbemtime_getdmtfnonntfs.htm
tech.root: wmi
ms.assetid: 40353352-da1f-44d8-a2c3-e6fd4639bd98
ms.date: 12/05/2018
ms.keywords: ?GetDMTFNonNtfs@WBEMTime@@QBEPAGXZ, ?GetDMTFNonNtfs@WBEMTime@@QEBAPEAGXZ, GetDMTFNonNtfs, GetDMTFNonNtfs method [Windows Management Instrumentation], GetDMTFNonNtfs method [Windows Management Instrumentation],WBEMTime interface, WBEMTime interface [Windows Management Instrumentation],GetDMTFNonNtfs method, WBEMTime.GetDMTFNonNtfs, WBEMTime::GetDMTFNonNtfs, _hmm_wbemtime_getdmtfnonntfs, wbemtime/WBEMTime::GetDMTFNonNtfs, wmi.wbemtime_getdmtfnonntfs
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
 - WBEMTime::GetDMTFNonNtfs
 - wbemtime/WBEMTime::GetDMTFNonNtfs
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
 - WBEMTime.GetDMTFNonNtfs
 - ?GetDMTFNonNtfs@WBEMTime@@QBEPAGXZ
 - ?GetDMTFNonNtfs@WBEMTime@@QEBAPEAGXZ
---

# WBEMTime::GetDMTFNonNtfs


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetDMTFNonNtfs</b> method gets a DMTF date in a 
CIM <a href="/windows/desktop/WmiSdk/date-and-time-format">Date and Time Format</a> from a FAT that does not have time zones.



## -returns

Returns a <b>BSTR</b> in <a href="/windows/desktop/WmiSdk/date-and-time-format">Date and Time Format</a>.

## -remarks

The calling function must call <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> on the return value.

The time property of <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> is held in GMT. The <b>GetDMTFNonNtfs</b> method adjusts this time to local time, converts it to a DMTF string, and sets the UTC to "***".  This is compatible with the Microsoft Windows API methods which return time without being time-zone aware.
