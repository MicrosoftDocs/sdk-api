---
UID: NF:wbemtime.WBEMTimeSpan.operator-assign(const FILETIME &)
title: WBEMTimeSpan::operator-assign(const FILETIME &)
author: windows-sdk-content
description: Converts a BSTR time interval value to a WBEMTimeSpan object in CIM date and time format.
old-location: wmi\wbemtimespan_operator_equal.htm
tech.root: WmiSdk
ms.assetid: e97bf5c7-90fd-49a7-9c3c-c719d5374f84
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: WBEMTimeSpan interface [Windows Management Instrumentation],operator= method, WBEMTimeSpan.operator-assign(const FILETIME &), WBEMTimeSpan.operator=, WBEMTimeSpan::operator-assign(const FILETIME &), WBEMTimeSpan::operator=, _hmm_wbemtimespan_operator_equal, operator=, operator= method [Windows Management Instrumentation], operator= method [Windows Management Instrumentation],WBEMTimeSpan interface, wbemtime/WBEMTimeSpan::operator=, wmi.wbemtimespan_operator_equal
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
 - WBEMTimeSpan.operator=
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WBEMTimeSpan::operator-assign(const FILETIME &)


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/bcec87c1-32ba-451b-92bb-80c8a5007adb">WBEMTimeSpan</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

Converts a <b>BSTR</b> time interval value to a <a href="https://msdn.microsoft.com/bcec87c1-32ba-451b-92bb-80c8a5007adb">WBEMTimeSpan</a> object in CIM <a href="https://msdn.microsoft.com/be239bf8-88a3-47bc-ae4f-49a5195e7a7d">date and time format</a>.


## -parameters




### -param ft

TBD




#### - bstrDMTFFormat

<b>BSTR</b> in <a href="https://msdn.microsoft.com/13a3ca74-e3e9-44d7-9254-e288eb70ae4c">Interval Format</a>.

