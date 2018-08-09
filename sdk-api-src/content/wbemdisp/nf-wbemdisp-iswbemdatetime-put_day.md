---
UID: NF:wbemdisp.ISWbemDateTime.put_Day
title: ISWbemDateTime::put_Day
author: windows-sdk-content
description: Gets or sets a value that represents the day component of the datetime value.
old-location: wmi\swbemdatetime_day.htm
old-project: WmiSdk
ms.assetid: 60da99bc-560c-45bc-b787-f4bef8e5a509
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: Day property [Windows Management Instrumentation], Day property [Windows Management Instrumentation],ISWbemDateTime interface, Day property [Windows Management Instrumentation],SWbemDateTime object, ISWbemDateTime interface [Windows Management Instrumentation],Day property, ISWbemDateTime.get_Day, ISWbemDateTime.put_Day, ISWbemDateTime::put_Day, SWbemDateTime object [Windows Management Instrumentation],Day property, SWbemDateTime.Day, _hmm_swbemdatetime.day, put_Day, wmi.swbemdatetime_day
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
 - SWbemDateTime.Day
 - ISWbemDateTime.Day
 - ISWbemDateTime.get_Day
 - ISWbemDateTime.put_Day
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemDateTime::put_Day


## -description


The 
<b>Day</b> property of the 
<a href="https://msdn.microsoft.com/3dd34c73-3c2b-4d59-827b-169cf8020213">SWbemDateTime</a> object gets or sets a value that represents the day component of the datetime value. The value must be in the range of 1 through 31 if <a href="https://msdn.microsoft.com/ba5fcf17-7c26-4960-9da9-e380d90e5f3e">IsInterval</a> is <b>FALSE</b>. However, error checking is not sensitive to the month value.  Thus, the in-range value of 31 will not return an error in the cases where the <a href="https://msdn.microsoft.com/05818f0a-7e15-4ddd-a6a7-9d16ae82cd3c">SWbemDateTime.Month</a> value is for a month of fewer than 31 days (February, April, June, September, November).

The default value for 
<b>Day</b> is 01.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.

This property is read/write.


## -parameters


## -see-also




<a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">DATETIME</a>



<a href="https://msdn.microsoft.com/3dd34c73-3c2b-4d59-827b-169cf8020213">SWbemDateTime</a>



<a href="https://msdn.microsoft.com/a713378b-3953-49d8-9c6a-44aa9337eae2">SWbemDateTime.DaySpecified</a>
 

 

