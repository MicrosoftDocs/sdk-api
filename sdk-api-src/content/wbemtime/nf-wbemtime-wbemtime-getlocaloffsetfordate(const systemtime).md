---
UID: NF:wbemtime.WBEMTime.GetLocalOffsetForDate(const SYSTEMTIME)
title: WBEMTime::GetLocalOffsetForDate(const SYSTEMTIME)
author: windows-sdk-content
description: The GetLocalOffsetForDate method returns the offset in minutes (+ or &#8211;) between GMT and local time for the SYSTEMTIME supplied in the argument.
old-location: wmi\wbemtime_getlocaloffsetfordate_const_systemtime__.htm
tech.root: WmiSdk
ms.assetid: efb25bb5-7a3e-4d80-ab5f-fd47cc5c83b7
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: "?GetLocalOffsetForDate@WBEMTime@@SGJPBU_SYSTEMTIME@@@Z, GetLocalOffsetForDate, GetLocalOffsetForDate method [Windows Management Instrumentation], GetLocalOffsetForDate method [Windows Management Instrumentation],WBEMTime interface, WBEMTime interface [Windows Management Instrumentation],GetLocalOffsetForDate method, WBEMTime.GetLocalOffsetForDate, WBEMTime.GetLocalOffsetForDate(const SYSTEMTIME), WBEMTime::GetLocalOffsetForDate, WBEMTime::GetLocalOffsetForDate(const SYSTEMTIME), WBEMTime::GetLocalOffsetForDate(const SYSTEMTIME*), wbemtime/WBEMTime::GetLocalOffsetForDate, wmi.wbemtime_getlocaloffsetfordate_const_systemtime__"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - WBEMTime.GetLocalOffsetForDate
 - ?GetLocalOffsetForDate@WBEMTime@@SGJPBU_SYSTEMTIME@@@Z
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WBEMTime::GetLocalOffsetForDate(const SYSTEMTIME)


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/b633bc8c-9d02-4bcf-8528-10773fb5ae7a">WBEMTime</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>GetLocalOffsetForDate</b> method returns the offset in minutes (+ or –) between GMT and local time for the <b>SYSTEMTIME</b> supplied in the argument.


## -parameters




### -param pst

Pointer to a MFC <b>SYSTEMTIME</b> structure that represents a date and time and using individual members for the month, day, year, weekday, hour, minute, second, and millisecond.


## -returns



Returns the offset in minutes (+ or -) between GMT and local time for the time supplied in the argument.




## -remarks



These are public static functions that  permit their usage anywhere without having a <a href="https://msdn.microsoft.com/b633bc8c-9d02-4bcf-8528-10773fb5ae7a">WBEMTime</a> object.



