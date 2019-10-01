---
UID: NF:wbemtime.WBEMTime.GetDMTFNonNtfs
title: WBEMTime::GetDMTFNonNtfs (wbemtime.h)
author: windows-sdk-content
description: The GetDMTFNonNtfs method gets a DMTF date in a CIM Date and Time Format from a FAT that does not have time zones.
old-location: wmi\wbemtime_getdmtfnonntfs.htm
tech.root: WmiSdk
ms.assetid: 40353352-da1f-44d8-a2c3-e6fd4639bd98
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "?GetDMTFNonNtfs@WBEMTime@@QBEPAGXZ, ?GetDMTFNonNtfs@WBEMTime@@QEBAPEAGXZ, GetDMTFNonNtfs, GetDMTFNonNtfs method [Windows Management Instrumentation], GetDMTFNonNtfs method [Windows Management Instrumentation],WBEMTime interface, WBEMTime interface [Windows Management Instrumentation],GetDMTFNonNtfs method, WBEMTime.GetDMTFNonNtfs, WBEMTime::GetDMTFNonNtfs, _hmm_wbemtime_getdmtfnonntfs, wbemtime/WBEMTime::GetDMTFNonNtfs, wmi.wbemtime_getdmtfnonntfs"
ms.topic: method
f1_keywords: 
 - "wbemtime/WBEMTime.GetDMTFNonNtfs"
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
 - WBEMTime.GetDMTFNonNtfs
 - ?GetDMTFNonNtfs@WBEMTime@@QBEPAGXZ
 - ?GetDMTFNonNtfs@WBEMTime@@QEBAPEAGXZ
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WBEMTime::GetDMTFNonNtfs


## -description


<p class="CCE_Message">[The <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetDMTFNonNtfs</b> method gets a DMTF date in a 
CIM <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/date-and-time-format">Date and Time Format</a> from a FAT that does not have time zones.


## -parameters






## -returns



Returns a <b>BSTR</b> in <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/date-and-time-format">Date and Time Format</a>.




## -remarks



The calling function must call <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> on the return value.

The time property of <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> is held in GMT. The <b>GetDMTFNonNtfs</b> method adjusts this time to local time, converts it to a DMTF string, and sets the UTC to "***".  This is compatible with the Microsoft Windows API methods which return time without being time-zone aware.



