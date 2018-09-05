---
UID: NF:wbemtime.WBEMTimeSpan.GetBSTR
title: WBEMTimeSpan::GetBSTR
author: windows-sdk-content
description: The GetBSTR method gets the time span as a BSTR in Date and Time format.
old-location: wmi\wbemtimespan_getbstr.htm
old-project: WmiSdk
ms.assetid: f5db5a7a-0590-4598-bde7-e90cfc7cd932
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: GetBSTR, GetBSTR method [Windows Management Instrumentation], GetBSTR method [Windows Management Instrumentation],WBEMTimeSpan interface, WBEMTimeSpan interface [Windows Management Instrumentation],GetBSTR method, WBEMTimeSpan.GetBSTR, WBEMTimeSpan::GetBSTR, _hmm_wbemtimespan_getbstr, wbemtime/WBEMTimeSpan::GetBSTR, wmi.wbemtimespan_getbstr
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
 - WBEMTimeSpan.GetBSTR
product: Windows
targetos: Windows
req.lib: 
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WBEMTimeSpan::GetBSTR


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/bcec87c1-32ba-451b-92bb-80c8a5007adb">WBEMTimeSpan</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>GetBSTR</b> method gets the time span as a <b>BSTR</b> in <a href="https://msdn.microsoft.com/be239bf8-88a3-47bc-ae4f-49a5195e7a7d">Date and Time format</a>.


## -parameters






## -returns



The time span is returned as a <b>BSTR</b> in <a href="https://msdn.microsoft.com/be239bf8-88a3-47bc-ae4f-49a5195e7a7d">Date and Time Format</a>.




## -remarks



The calling method must call <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> on the return value.



