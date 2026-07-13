---
UID: NF:wbemtime.WBEMTime.GetLocalOffsetForDate(constFILETIME)
title: WBEMTime::GetLocalOffsetForDate(const FILETIME) (wbemtime.h)
description: The GetLocalOffsetForDate method returns the offset in minutes (+ or —) between GMT and local time for the FILETIME supplied in the argument. (overload 1/4)
helpviewer_keywords: ["GetLocalOffsetForDate","GetLocalOffsetForDate method [Windows Management Instrumentation]","GetLocalOffsetForDate method [Windows Management Instrumentation]","WBEMTime interface","WBEMTime interface [Windows Management Instrumentation]","GetLocalOffsetForDate method","WBEMTime.GetLocalOffsetForDate","WBEMTime.GetLocalOffsetForDate(const FILETIME)","WBEMTime::GetLocalOffsetForDate","WBEMTime::GetLocalOffsetForDate(const FILETIME)","WBEMTime::GetLocalOffsetForDate(const FILETIME*)","wbemtime/WBEMTime::GetLocalOffsetForDate","wmi.wbemtime_getlocaloffsetfordate_const_filetime__"]
old-location: wmi\wbemtime_getlocaloffsetfordate_const_filetime__.htm
tech.root: wmi
ms.assetid: fd40907d-c4df-4eb0-8516-45def3d5d01f
ms.date: 12/05/2018
ms.keywords: GetLocalOffsetForDate, GetLocalOffsetForDate method [Windows Management Instrumentation], GetLocalOffsetForDate method [Windows Management Instrumentation],WBEMTime interface, WBEMTime interface [Windows Management Instrumentation],GetLocalOffsetForDate method, WBEMTime.GetLocalOffsetForDate, WBEMTime.GetLocalOffsetForDate(const FILETIME), WBEMTime::GetLocalOffsetForDate, WBEMTime::GetLocalOffsetForDate(const FILETIME), WBEMTime::GetLocalOffsetForDate(const FILETIME*), wbemtime/WBEMTime::GetLocalOffsetForDate, wmi.wbemtime_getlocaloffsetfordate_const_filetime__
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
 - WBEMTime::GetLocalOffsetForDate
 - wbemtime/WBEMTime::GetLocalOffsetForDate
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
 - WBEMTime.GetLocalOffsetForDate
---

# WBEMTime::GetLocalOffsetForDate(const FILETIME)


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetLocalOffsetForDate</b> method returns the offset in minutes (+ or –) between GMT and local time for the FILETIME supplied in the argument.

## -parameters

### -param pft

TBD




#### - tmin

Pointer to a MFC <b>FILETIME</b> structure that represents the number of 100-nanosecond intervals since January 1, 1601 as a 64-bit value.

## -returns

Returns the offset in minutes (+ or -) between GMT and local time for the time supplied in the argument.

## -remarks

These are public static functions which permit their usage anywhere without having a <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> object.
