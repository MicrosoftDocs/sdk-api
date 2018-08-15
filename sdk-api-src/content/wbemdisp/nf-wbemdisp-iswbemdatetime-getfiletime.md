---
UID: NF:wbemdisp.ISWbemDateTime.GetFileTime
title: ISWbemDateTime::GetFileTime
author: windows-sdk-content
description: Converts a date and time value in the CIM DATETIME format to the FILETIME format.
old-location: wmi\swbemdatetime_getfiletime.htm
old-project: WmiSdk
ms.assetid: 08e0761d-e735-454a-8429-2bd1eb331123
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: GetFileTime, GetFileTime method [Windows Management Instrumentation], GetFileTime method [Windows Management Instrumentation],ISWbemDateTime interface, GetFileTime method [Windows Management Instrumentation],SWbemDateTime object, ISWbemDateTime interface [Windows Management Instrumentation],GetFileTime method, ISWbemDateTime.GetFileTime, ISWbemDateTime::GetFileTime, SWbemDateTime object [Windows Management Instrumentation],GetFileTime method, SWbemDateTime.GetFileTime, _hmm_swbemdatetime.getfiletime, wmi.swbemdatetime_getfiletime
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
 - SWbemDateTime.GetFileTime
 - ISWbemDateTime.GetFileTime
 - ISWbemDateTime.GetFileTime
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemDateTime::GetFileTime


## -description


The 
<b>GetFileTime</b> method of the 
<a href="https://msdn.microsoft.com/3dd34c73-3c2b-4d59-827b-169cf8020213">SWbemDateTime</a> object converts a date and time value in the CIM <a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">DATETIME</a> format to the FILETIME  format.

If the parameter is set to <b>TRUE</b>, then the return value represents a local time for the client. Otherwise, the return value is a Coordinated Universal Time (UTC) time. A <b>FILETIME</b> <a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">DATETIME</a> structure is a 64-bit value that represents the number of 100-nanosecond units since the beginning of January 1, 1601.
Windows Management Instrumentation (WMI) treats <b>FILETIME</b> values as string representations of unsigned 64-bit numbers.

For  an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param bIsLocal




### -param strFileTime






#### - bIsLocaL [in, optional]

Indicates whether the returned value is interpreted as local time. The UTC property then contains the local time converted to the correct Coordinated Universal Times (UTC) offset. If the value is <b>FALSE</b>, then the value is interpreted as UTC with a zero (0) offset.


## -returns



The date and time in the <b>FILETIME</b> format.




## -remarks



<b>VT_DATE</b> and <b>FILETIME</b> values cannot contain wildcard fields.

The 
<b>GetFileTime</b> method fails (wbemErrFailed) if any of the following properties are <b>FALSE</b>:

<ul>
<li>
<a href="https://msdn.microsoft.com/afac0a08-7bd0-42f1-b5a7-8664f9db8615">YearSpecified</a>
</li>
<li>
<a href="https://msdn.microsoft.com/12dd94de-24be-4b13-bde5-2fc28be94efa">MonthSpecified</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a713378b-3953-49d8-9c6a-44aa9337eae2">DaySpecified</a>
</li>
<li>
<a href="https://msdn.microsoft.com/55211da6-cbd5-4e61-ab7d-ee20363e9d81">HoursSpecified</a>
</li>
<li>
<a href="https://msdn.microsoft.com/de15f87e-0092-467e-b0d7-42ef447fa00a">MinutesSpecified</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9f9b75c3-ae08-49a6-b747-294831601a62">SecondsSpecified</a>
</li>
<li>
<a href="https://msdn.microsoft.com/65244ece-2326-4edc-b982-57e2046ec33e">MicrosecondsSpecified</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9cb04351-294b-48ba-8d1c-2f28cb9ce463">UTCSpecified</a>
</li>
</ul>
On a successful return from 
<a href="https://msdn.microsoft.com/e375afda-5e94-46d6-b1ac-e801e0f4a620">SetFileTime</a>, all of these properties are set to <b>TRUE</b>.


#### Examples

For examples of using the <a href="https://msdn.microsoft.com/3dd34c73-3c2b-4d59-827b-169cf8020213">SWbemDateTime</a> object to 
     convert CIM <a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">DATETIME</a> values to and from either the 
     <b>FILETIME</b> format or the <b>VT_DATE</b> format, see <a href="https://msdn.microsoft.com/dd01a732-5c88-4c24-a551-4d5452e712cc">WMI Tasks: Dates and Times</a>. For a description of the CIM <b>DATETIME</b> format, see <a href="https://msdn.microsoft.com/be239bf8-88a3-47bc-ae4f-49a5195e7a7d">Date and Time Format</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">DATETIME</a>



<a href="https://msdn.microsoft.com/3dd34c73-3c2b-4d59-827b-169cf8020213">SWbemDateTime</a>



<a href="https://msdn.microsoft.com/e63e7acc-89d4-458a-a1ab-4d4a65cf7f8b">SWbemDateTime.GetVarDate</a>
 

 

