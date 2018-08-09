---
UID: NF:wbemdisp.ISWbemDateTime.put_DaySpecified
title: ISWbemDateTime::put_DaySpecified
author: windows-sdk-content
description: Boolean value that indicates whether the day component in the CIM DATETIME value contains an interval or a wildcard value.
old-location: wmi\swbemdatetime_dayspecified.htm
old-project: WmiSdk
ms.assetid: a713378b-3953-49d8-9c6a-44aa9337eae2
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: DaySpecified property [Windows Management Instrumentation], DaySpecified property [Windows Management Instrumentation],ISWbemDateTime interface, DaySpecified property [Windows Management Instrumentation],SWbemDateTime object, ISWbemDateTime interface [Windows Management Instrumentation],DaySpecified property, ISWbemDateTime.get_DaySpecified, ISWbemDateTime.put_DaySpecified, ISWbemDateTime::put_DaySpecified, SWbemDateTime object [Windows Management Instrumentation],DaySpecified property, SWbemDateTime.DaySpecified, _hmm_swbemdatetime.dayspecified, put_DaySpecified, wmi.swbemdatetime_dayspecified
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
 - SWbemDateTime.DaySpecified
 - ISWbemDateTime.DaySpecified
 - ISWbemDateTime.get_DaySpecified
 - ISWbemDateTime.put_DaySpecified
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemDateTime::put_DaySpecified


## -description


The 
<b>DaySpecified</b> property of the 
<a href="https://msdn.microsoft.com/3dd34c73-3c2b-4d59-827b-169cf8020213">SWbemDateTime</a> object is a Boolean value that indicates whether the day component in the CIM <a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">DATETIME</a> value contains an interval or a wildcard value. If 
<b>DaySpecified</b> is <b>TRUE</b> and 
<a href="https://msdn.microsoft.com/ba5fcf17-7c26-4960-9da9-e380d90e5f3e">IsInterval</a> is <b>FALSE</b>, then 
<a href="https://msdn.microsoft.com/60da99bc-560c-45bc-b787-f4bef8e5a509">SWbemDateTime.Day</a> contains a datetime value. A <a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">DATETIME</a> value that contains an interval cannot be converted into either the <b>VT_DATE</b> format or the <b>FILETIME</b> format. If 
<b>DaySpecified</b> is <b>FALSE</b> and 
<b>IsInterval</b> is <b>TRUE</b>, then <b>SWbemDateTime.Day</b> contains an interval.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.

This property is read/write.


## -parameters


## -see-also




<a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">DATETIME</a>



<a href="https://msdn.microsoft.com/3dd34c73-3c2b-4d59-827b-169cf8020213">SWbemDateTime</a>



<a href="https://msdn.microsoft.com/60da99bc-560c-45bc-b787-f4bef8e5a509">SWbemDateTime.Day</a>
 

 

