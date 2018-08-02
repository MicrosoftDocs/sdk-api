---
UID: NF:wbemdisp.ISWbemDateTime.get_SecondsSpecified
title: ISWbemDateTime::get_SecondsSpecified
author: windows-sdk-content
description: Boolean value that indicates whether the seconds component in the CIM DATETIME value contains an interval or a wildcard value.
old-location: wmi\swbemdatetime_secondsspecified.htm
old-project: WmiSdk
ms.assetid: 9f9b75c3-ae08-49a6-b747-294831601a62
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ISWbemDateTime interface [Windows Management Instrumentation],SecondsSpecified property, ISWbemDateTime.get_SecondsSpecified, ISWbemDateTime.put_SecondsSpecified, ISWbemDateTime::get_SecondsSpecified, SWbemDateTime object [Windows Management Instrumentation],SecondsSpecified property, SWbemDateTime.SecondsSpecified, SecondsSpecified property [Windows Management Instrumentation], SecondsSpecified property [Windows Management Instrumentation],ISWbemDateTime interface, SecondsSpecified property [Windows Management Instrumentation],SWbemDateTime object, _hmm_swbemdatetime.secondsspecified, get_SecondsSpecified, wmi.swbemdatetime_secondsspecified
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
 - SWbemDateTime.SecondsSpecified
 - ISWbemDateTime.SecondsSpecified
 - ISWbemDateTime.get_SecondsSpecified
 - ISWbemDateTime.put_SecondsSpecified
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemDateTime::get_SecondsSpecified


## -description


The 
<b>SecondsSpecified</b> property of the 
<a href="https://msdn.microsoft.com/3dd34c73-3c2b-4d59-827b-169cf8020213">SWbemDateTime</a> object is a Boolean value that indicates whether the seconds component in the CIM <a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">DATETIME</a> value contains an interval or a wildcard value. If 
<b>SecondsSpecified</b> is <b>TRUE</b> and 
<a href="https://msdn.microsoft.com/ba5fcf17-7c26-4960-9da9-e380d90e5f3e">IsInterval</a> is <b>FALSE</b>, then 
<a href="https://msdn.microsoft.com/194d4309-6abf-4c5f-99f8-60d2c835af6c">SWbemDateTime.Seconds</a> contains a date value. A datetime value that contains an interval cannot be converted into either the <b>VT_DATE</b> format or the <b>FILETIME</b> format. If 
<b>SecondsSpecified</b> is <b>FALSE</b> and 
<b>IsInterval</b> is <b>TRUE</b>, then <b>SWbemDateTime.Seconds</b> contains an interval.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.

This property is read/write.


## -parameters


## -see-also




<a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">DATETIME</a>



<a href="https://msdn.microsoft.com/3dd34c73-3c2b-4d59-827b-169cf8020213">SWbemDateTime</a>



<a href="https://msdn.microsoft.com/194d4309-6abf-4c5f-99f8-60d2c835af6c">SWbemDateTime.Seconds</a>
 

 

