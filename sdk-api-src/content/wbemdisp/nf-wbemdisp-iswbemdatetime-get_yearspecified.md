---
UID: NF:wbemdisp.ISWbemDateTime.get_YearSpecified
title: ISWbemDateTime::get_YearSpecified
author: windows-sdk-content
description: Boolean value that indicates whether the year component in the CIM datetime value contains an interval or a wildcard value.
old-location: wmi\swbemdatetime_yearspecified.htm
old-project: WmiSdk
ms.assetid: afac0a08-7bd0-42f1-b5a7-8664f9db8615
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: ISWbemDateTime interface [Windows Management Instrumentation],YearSpecified property, ISWbemDateTime.get_YearSpecified, ISWbemDateTime.put_YearSpecified, ISWbemDateTime::get_YearSpecified, SWbemDateTime object [Windows Management Instrumentation],YearSpecified property, SWbemDateTime.YearSpecified, YearSpecified property [Windows Management Instrumentation], YearSpecified property [Windows Management Instrumentation],ISWbemDateTime interface, YearSpecified property [Windows Management Instrumentation],SWbemDateTime object, _hmm_swbemdatetime.yearspecified, get_YearSpecified, wmi.swbemdatetime_yearspecified
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
 - SWbemDateTime.YearSpecified
 - ISWbemDateTime.YearSpecified
 - ISWbemDateTime.get_YearSpecified
 - ISWbemDateTime.put_YearSpecified
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemDateTime::get_YearSpecified


## -description


The 
<b>YearSpecified</b> property of the 
<a href="https://msdn.microsoft.com/3dd34c73-3c2b-4d59-827b-169cf8020213">SWbemDateTime</a> object is a Boolean value that indicates whether the year component in the CIM datetime value contains an interval or a wildcard value. If 
<b>YearSpecified</b> is <b>TRUE</b> and 
<a href="https://msdn.microsoft.com/ba5fcf17-7c26-4960-9da9-e380d90e5f3e">IsInterval</a> is <b>FALSE</b>, then 
<a href="https://msdn.microsoft.com/eab3738a-c92a-4602-b1ee-e2547da88308">SWbemDateTime.Year</a> contains a datetime value. A datetime value that contains an interval cannot be converted into either the  <b>VT_DATE</b> format or the <b>FILETIME</b> format. If 
<b>YearSpecified</b> is <b>FALSE</b> and 
<b>IsInterval</b> is <b>TRUE</b>, then <b>SWbemDateTime.Year</b> contains an interval.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.

This property is read/write.


## -parameters


## -see-also




<a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">DATETIME</a>



<a href="https://msdn.microsoft.com/3dd34c73-3c2b-4d59-827b-169cf8020213">SWbemDateTime</a>



<a href="https://msdn.microsoft.com/eab3738a-c92a-4602-b1ee-e2547da88308">SWbemDateTime.Year</a>
 

 

