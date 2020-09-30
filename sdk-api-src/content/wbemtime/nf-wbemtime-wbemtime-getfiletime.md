---
UID: NF:wbemtime.WBEMTime.GetFILETIME
title: WBEMTime::GetFILETIME (wbemtime.h)
description: The GetFILETIME method gets the time as an MFC FILETIME structure.
helpviewer_keywords: ["?GetFILETIME@WBEMTime@@QBEHPAU_FILETIME@@@Z","GetFILETIME","GetFILETIME method [Windows Management Instrumentation]","GetFILETIME method [Windows Management Instrumentation]","WBEMTime interface","WBEMTime interface [Windows Management Instrumentation]","GetFILETIME method","WBEMTime.GetFILETIME","WBEMTime::GetFILETIME","_hmm_wbemtime_getfiletime","wbemtime/WBEMTime::GetFILETIME","wmi.wbemtime_getfiletime"]
old-location: wmi\wbemtime_getfiletime.htm
tech.root: wmi
ms.assetid: 3debc121-ff7b-4e2c-9d77-502ee491cad8
ms.date: 12/05/2018
ms.keywords: ?GetFILETIME@WBEMTime@@QBEHPAU_FILETIME@@@Z, GetFILETIME, GetFILETIME method [Windows Management Instrumentation], GetFILETIME method [Windows Management Instrumentation],WBEMTime interface, WBEMTime interface [Windows Management Instrumentation],GetFILETIME method, WBEMTime.GetFILETIME, WBEMTime::GetFILETIME, _hmm_wbemtime_getfiletime, wbemtime/WBEMTime::GetFILETIME, wmi.wbemtime_getfiletime
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
 - WBEMTime::GetFILETIME
 - wbemtime/WBEMTime::GetFILETIME
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
 - WBEMTime.GetFILETIME
 - ?GetFILETIME@WBEMTime@@QBEHPAU_FILETIME@@@Z
---

# WBEMTime::GetFILETIME


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetFILETIME</b> method gets the time as an MFC <b>FILETIME</b> structure.

## -parameters

### -param pst

MFC <b>FILETIME</b> structure. The <b>FILETIME</b> structure is a 64-bit value that represents the number of 100-nanosecond intervals since January 1, 1601.

## -returns

The method returns <b>TRUE</b> if the time is valid and <b>FALSE</b> if the time is not valid. If <b>FALSE</b> is returned, the value of <i>pst</i> is indeterminate.