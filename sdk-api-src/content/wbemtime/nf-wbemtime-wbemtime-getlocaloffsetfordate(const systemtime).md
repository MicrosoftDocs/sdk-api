---
UID: NF:wbemtime.WBEMTime.GetLocalOffsetForDate(const SYSTEMTIME)
title: WBEMTime::GetLocalOffsetForDate(const SYSTEMTIME)
author: windows-sdk-content
description: The GetLocalOffsetForDate method returns the offset in minutes (+ or &#8211;) between GMT and local time for the FILETIME supplied in the argument.
old-location: wmi\wbemtime_getlocaloffsetfordate_const_filetime__.htm
old-project: WmiSdk
ms.assetid: fd40907d-c4df-4eb0-8516-45def3d5d01f
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: GetLocalOffsetForDate, GetLocalOffsetForDate method [Windows Management Instrumentation], GetLocalOffsetForDate method [Windows Management Instrumentation],WBEMTime interface, WBEMTime interface [Windows Management Instrumentation],GetLocalOffsetForDate method, WBEMTime.GetLocalOffsetForDate, WBEMTime.GetLocalOffsetForDate(const SYSTEMTIME), WBEMTime::GetLocalOffsetForDate, WBEMTime::GetLocalOffsetForDate(const FILETIME*), WBEMTime::GetLocalOffsetForDate(const SYSTEMTIME), wbemtime/WBEMTime::GetLocalOffsetForDate, wmi.wbemtime_getlocaloffsetfordate_const_filetime__
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemtime.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WbemTimeout
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
product: Windows
targetos: Windows
req.lib: 
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WBEMTime::GetLocalOffsetForDate(const SYSTEMTIME)


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/b633bc8c-9d02-4bcf-8528-10773fb5ae7a">WBEMTime</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>GetLocalOffsetForDate</b> method returns the offset in minutes (+ or –) between GMT and local time for the FILETIME supplied in the argument.


## -parameters




### -param pst






#### - pft

Pointer to a MFC <b>FILETIME</b> structure that represents the number of 100-nanosecond intervals since January 1, 1601 as a 64-bit value.


## -returns



Returns the offset in minutes (+ or -) between GMT and local time for the time supplied in the argument.




## -remarks



These are public static functions which permit their usage anywhere without having a <a href="https://msdn.microsoft.com/b633bc8c-9d02-4bcf-8528-10773fb5ae7a">WBEMTime</a> object.



