---
UID: NF:wbemdisp.ISWbemDateTime.put_HoursSpecified
title: ISWbemDateTime::put_HoursSpecified
author: windows-sdk-content
description: The HoursSpecified property of the SWbemDateTime object is a Boolean value that indicates whether the hours component in the CIM datetime value contains an interval or a wildcard value.
old-location: wmi\swbemdatetime_hoursspecified.htm
old-project: WmiSdk
ms.assetid: 55211da6-cbd5-4e61-ab7d-ee20363e9d81
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: HoursSpecified property [Windows Management Instrumentation], HoursSpecified property [Windows Management Instrumentation],ISWbemDateTime interface, HoursSpecified property [Windows Management Instrumentation],SWbemDateTime object, ISWbemDateTime interface [Windows Management Instrumentation],HoursSpecified property, ISWbemDateTime.get_HoursSpecified, ISWbemDateTime.put_HoursSpecified, ISWbemDateTime::put_HoursSpecified, SWbemDateTime object [Windows Management Instrumentation],HoursSpecified property, SWbemDateTime.HoursSpecified, _hmm_swbemdatetime.hoursspecified, put_HoursSpecified, wmi.swbemdatetime_hoursspecified
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemdisp.h
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
 - SWbemDateTime.HoursSpecified
 - ISWbemDateTime.HoursSpecified
 - ISWbemDateTime.get_HoursSpecified
 - ISWbemDateTime.put_HoursSpecified
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemDateTime::put_HoursSpecified


## -description


The 
<b>HoursSpecified</b> property of the 
<a href="https://msdn.microsoft.com/3dd34c73-3c2b-4d59-827b-169cf8020213">SWbemDateTime</a> object is a Boolean value that indicates whether the hours component in the CIM datetime value contains an interval or a wildcard value. If 
<b>HoursSpecified</b> is <b>TRUE</b> and 
<a href="https://msdn.microsoft.com/ba5fcf17-7c26-4960-9da9-e380d90e5f3e">IsInterval</a> is <b>FALSE</b>, then 
<a href="https://msdn.microsoft.com/83f084fa-57a5-4467-acea-7e19de82a91f">SWbemDateTime.Hours</a> contains a datetime value. A datetime value that contains an interval cannot be converted into either the <b>VT_DATE</b> format or the <b>FILETIME</b> format. If 
<b>HoursSpecified</b> is <b>FALSE</b> and 
<b>IsInterval</b> is <b>TRUE</b>, then <b>SWbemDateTime.Hours</b> contains an interval.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.

This property is read/write.


## -parameters


## -see-also




<a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">DATETIME</a>



<a href="https://msdn.microsoft.com/3dd34c73-3c2b-4d59-827b-169cf8020213">SWbemDateTime</a>



<a href="https://msdn.microsoft.com/83f084fa-57a5-4467-acea-7e19de82a91f">SWbemDateTime.Hours</a>
 

 

