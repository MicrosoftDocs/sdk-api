---
UID: NF:wbemdisp.ISWbemDateTime.put_Minutes
title: ISWbemDateTime::put_Minutes
author: windows-sdk-content
description: Gets or sets a value that represents the minutes component of the datetime value.
old-location: wmi\swbemdatetime_minutes.htm
old-project: WmiSdk
ms.assetid: a52a66c2-f7ab-48d0-bdee-a07984ed3bc2
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: ISWbemDateTime interface [Windows Management Instrumentation],Minutes property, ISWbemDateTime.get_Minutes, ISWbemDateTime.put_Minutes, ISWbemDateTime::put_Minutes, Minutes property [Windows Management Instrumentation], Minutes property [Windows Management Instrumentation],ISWbemDateTime interface, Minutes property [Windows Management Instrumentation],SWbemDateTime object, SWbemDateTime object [Windows Management Instrumentation],Minutes property, SWbemDateTime.Minutes, _hmm_swbemdatetime.minutes, put_Minutes, wmi.swbemdatetime_minutes
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
 - SWbemDateTime.Minutes
 - ISWbemDateTime.Minutes
 - ISWbemDateTime.get_Minutes
 - ISWbemDateTime.put_Minutes
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemDateTime::put_Minutes


## -description


The 
<b>Minutes</b> property of the 
<a href="https://msdn.microsoft.com/3dd34c73-3c2b-4d59-827b-169cf8020213">SWbemDateTime</a> object gets or sets a value that represents the minutes component of the datetime value.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.

This property is read/write.


## -parameters


## -remarks



If the <b>SWbemDateTime.Minutes</b> property is set to 1, then the 
<a href="https://msdn.microsoft.com/194d4309-6abf-4c5f-99f8-60d2c835af6c">SWbemDateTime.Seconds</a> property contains a value that is offset by one second a rounding error that occurs when a CIM <b>datetime</b> value is translated to a <b>VT_DATE</b> value. If the 
<b>Minutes</b> property is set to 0 instead, then the 
<b>Seconds</b> property returns the correct value.


#### Examples

For examples of using the <a href="https://msdn.microsoft.com/3dd34c73-3c2b-4d59-827b-169cf8020213">SWbemDateTime</a>object to  convert CIM <a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">DATETIME</a> values to and from either the <b>FILETIME</b> format or the <b>VT_DATE</b> format, see <a href="https://msdn.microsoft.com/dd01a732-5c88-4c24-a551-4d5452e712cc">WMI Tasks: Dates and Times</a>. For a description of the CIM <b>DATETIME</b> format, see <a href="https://msdn.microsoft.com/be239bf8-88a3-47bc-ae4f-49a5195e7a7d">Date and Time Format</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">DATETIME</a>



<a href="https://msdn.microsoft.com/3dd34c73-3c2b-4d59-827b-169cf8020213">SWbemDateTime</a>



<a href="https://msdn.microsoft.com/de15f87e-0092-467e-b0d7-42ef447fa00a">SWbemDateTime.MinutesSpecified</a>
 

 

