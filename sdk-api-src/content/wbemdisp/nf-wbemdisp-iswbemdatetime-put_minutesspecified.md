---
UID: NF:wbemdisp.ISWbemDateTime.put_MinutesSpecified
title: ISWbemDateTime::put_MinutesSpecified
author: windows-sdk-content
description: Indicates whether the minutes component in the CIM datetime value contains an interval or a wildcard value.
old-location: wmi\swbemdatetime_minutesspecified.htm
old-project: WmiSdk
ms.assetid: de15f87e-0092-467e-b0d7-42ef447fa00a
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: ISWbemDateTime interface [Windows Management Instrumentation],MinutesSpecified property, ISWbemDateTime.get_MinutesSpecified, ISWbemDateTime.put_MinutesSpecified, ISWbemDateTime::put_MinutesSpecified, MinutesSpecified property [Windows Management Instrumentation], MinutesSpecified property [Windows Management Instrumentation],ISWbemDateTime interface, MinutesSpecified property [Windows Management Instrumentation],SWbemDateTime object, SWbemDateTime object [Windows Management Instrumentation],MinutesSpecified property, SWbemDateTime.MinutesSpecified, _hmm_swbemdatetime.minutesspecified, put_MinutesSpecified, wmi.swbemdatetime_minutesspecified
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
 - SWbemDateTime.MinutesSpecified
 - ISWbemDateTime.MinutesSpecified
 - ISWbemDateTime.get_MinutesSpecified
 - ISWbemDateTime.put_MinutesSpecified
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemDateTime::put_MinutesSpecified


## -description


The 
<b>MinutesSpecified</b> property of the 
<a href="https://msdn.microsoft.com/3dd34c73-3c2b-4d59-827b-169cf8020213">SWbemDateTime</a> object is a Boolean value that indicates whether the minutes component in the CIM datetime value contains an interval or a wildcard value. If 
<b>MinutesSpecified</b> is <b>TRUE</b> and 
<a href="https://msdn.microsoft.com/ba5fcf17-7c26-4960-9da9-e380d90e5f3e">IsInterval</a> is <b>FALSE</b> (indicating that the CIM datetime value has no wildcards), then 
<a href="https://msdn.microsoft.com/a52a66c2-f7ab-48d0-bdee-a07984ed3bc2">SWbemDateTime.Minutes</a> contains a date value. A datetime value that contains an interval cannot be converted into either the <b>VT_DATE</b> format or the <b>FILETIME</b> format. If 
<a href="https://msdn.microsoft.com/55211da6-cbd5-4e61-ab7d-ee20363e9d81">HoursSpecified</a> is <b>FALSE</b> and 
<b>IsInterval</b> is <b>TRUE</b>, then <b>SWbemDateTime.Minutes</b> contains an interval.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.

This property is read/write.


## -parameters


## -see-also




<a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">DATETIME</a>



<a href="https://msdn.microsoft.com/3dd34c73-3c2b-4d59-827b-169cf8020213">SWbemDateTime</a>



<a href="https://msdn.microsoft.com/a52a66c2-f7ab-48d0-bdee-a07984ed3bc2">SWbemDateTime.Minutes</a>
 

 

