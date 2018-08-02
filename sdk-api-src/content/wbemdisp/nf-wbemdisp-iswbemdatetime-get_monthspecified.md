---
UID: NF:wbemdisp.ISWbemDateTime.get_MonthSpecified
title: ISWbemDateTime::get_MonthSpecified
author: windows-sdk-content
description: Boolean value that indicates whether the month component in the CIM datetime value contains an interval or a wildcard value.
old-location: wmi\swbemdatetime_monthspecified.htm
old-project: WmiSdk
ms.assetid: 12dd94de-24be-4b13-bde5-2fc28be94efa
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ISWbemDateTime interface [Windows Management Instrumentation],MonthSpecified property, ISWbemDateTime.get_MonthSpecified, ISWbemDateTime.put_MonthSpecified, ISWbemDateTime::get_MonthSpecified, MonthSpecified property [Windows Management Instrumentation], MonthSpecified property [Windows Management Instrumentation],ISWbemDateTime interface, MonthSpecified property [Windows Management Instrumentation],SWbemDateTime object, SWbemDateTime object [Windows Management Instrumentation],MonthSpecified property, SWbemDateTime.MonthSpecified, _hmm_swbemdatetime.monthspecified, get_MonthSpecified, wmi.swbemdatetime_monthspecified
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemdisp.h
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
req.type-library: Wbemdisp.tlb
tech.root: 
req.typenames: WbemTimeout
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemdisp.dll
api_name:
 - SWbemDateTime.MonthSpecified
 - ISWbemDateTime.MonthSpecified
 - ISWbemDateTime.get_MonthSpecified
 - ISWbemDateTime.put_MonthSpecified
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemDateTime::get_MonthSpecified


## -description


The 
<b>MonthSpecified</b> property of the 
<a href="https://msdn.microsoft.com/3dd34c73-3c2b-4d59-827b-169cf8020213">SWbemDateTime</a> object is a Boolean value that indicates whether the month component in the CIM datetime value contains an interval or a wildcard value. If 
<b>MonthSpecified</b> is <b>TRUE</b> and 
<a href="https://msdn.microsoft.com/ba5fcf17-7c26-4960-9da9-e380d90e5f3e">IsInterval</a> is <b>FALSE</b>, then 
<a href="https://msdn.microsoft.com/05818f0a-7e15-4ddd-a6a7-9d16ae82cd3c">SWbemDateTime.Month</a> contains a date value. A datetime value that contains an interval cannot be converted into either the <b>VT_DATE</b> format or the <b>FILETIME</b> format. If 
<b>MonthSpecified</b> is <b>FALSE</b> and 
<b>IsInterval</b> is <b>TRUE</b>, then <b>SWbemDateTime.Month</b> contains an interval.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.

This property is read/write.


## -parameters


## -see-also




<a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">DATETIME</a>



<a href="https://msdn.microsoft.com/3dd34c73-3c2b-4d59-827b-169cf8020213">SWbemDateTime</a>



<a href="https://msdn.microsoft.com/05818f0a-7e15-4ddd-a6a7-9d16ae82cd3c">SWbemDateTime.Month</a>
 

 

