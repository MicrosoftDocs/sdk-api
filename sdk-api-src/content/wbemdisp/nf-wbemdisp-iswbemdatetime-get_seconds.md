---
UID: NF:wbemdisp.ISWbemDateTime.get_Seconds
title: ISWbemDateTime::get_Seconds
author: windows-sdk-content
description: Gets or sets a value that represents the seconds component of the datetime value.
old-location: wmi\swbemdatetime_seconds.htm
old-project: WmiSdk
ms.assetid: 194d4309-6abf-4c5f-99f8-60d2c835af6c
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: ISWbemDateTime interface [Windows Management Instrumentation],Seconds property, ISWbemDateTime.get_Seconds, ISWbemDateTime.put_Seconds, ISWbemDateTime::get_Seconds, SWbemDateTime object [Windows Management Instrumentation],Seconds property, SWbemDateTime.Seconds, Seconds property [Windows Management Instrumentation], Seconds property [Windows Management Instrumentation],ISWbemDateTime interface, Seconds property [Windows Management Instrumentation],SWbemDateTime object, _hmm_swbemdatetime.seconds, get_Seconds, wmi.swbemdatetime_seconds
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
 - SWbemDateTime.Seconds
 - ISWbemDateTime.Seconds
 - ISWbemDateTime.get_Seconds
 - ISWbemDateTime.put_Seconds
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemDateTime::get_Seconds


## -description


The 
<b>Seconds</b> property of the 
<a href="https://msdn.microsoft.com/3dd34c73-3c2b-4d59-827b-169cf8020213">SWbemDateTime</a> object gets or sets a value that represents the seconds component of the datetime value.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.

This property is read/write.


## -parameters


## -remarks



The <b>SWbemDateTime.Seconds</b> property may contain an incorrect value if the 
<a href="https://msdn.microsoft.com/a52a66c2-f7ab-48d0-bdee-a07984ed3bc2">SWbemDateTime.Minutes</a> property has been set to 1. It contains a value that is offset by one second  because of a rounding error that occurs when a CIM <a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">DATETIME</a> value is translated to a <b>VT_DATE</b> value. If the 
<b>Minutes</b> property is set to 0 (zero) instead, then the 
<b>Seconds</b> property returns the correct value.


#### Examples

For examples of using the <a href="https://msdn.microsoft.com/3dd34c73-3c2b-4d59-827b-169cf8020213">SWbemDateTime</a>object to  convert CIM <a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">DATETIME</a> values to and from either the <b>FILETIME</b> format or the  <b>VT_DATE</b> format, see <a href="https://msdn.microsoft.com/dd01a732-5c88-4c24-a551-4d5452e712cc">WMI Tasks: Dates and Times</a>. For a description of the CIM <b>DATETIME</b> format, see <a href="https://msdn.microsoft.com/be239bf8-88a3-47bc-ae4f-49a5195e7a7d">Date and Time Format</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">DATETIME</a>



<a href="https://msdn.microsoft.com/3dd34c73-3c2b-4d59-827b-169cf8020213">SWbemDateTime</a>



<a href="https://msdn.microsoft.com/9f9b75c3-ae08-49a6-b747-294831601a62">SWbemDateTime.SecondsSpecified</a>
 

 

