---
UID: NF:wbemdisp.ISWbemDateTime.GetVarDate
title: ISWbemDateTime::GetVarDate
author: windows-sdk-content
description: Converts a date and time value in the CIM DATETIME format to the VT_DATE format.
old-location: wmi\swbemdatetime_getvardate.htm
old-project: WmiSdk
ms.assetid: e63e7acc-89d4-458a-a1ab-4d4a65cf7f8b
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: GetVarDate, GetVarDate method [Windows Management Instrumentation], GetVarDate method [Windows Management Instrumentation],ISWbemDateTime interface, GetVarDate method [Windows Management Instrumentation],SWbemDateTime object, ISWbemDateTime interface [Windows Management Instrumentation],GetVarDate method, ISWbemDateTime.GetVarDate, ISWbemDateTime::GetVarDate, SWbemDateTime object [Windows Management Instrumentation],GetVarDate method, SWbemDateTime.GetVarDate, _hmm_swbemdatetime.getvardate, wmi.swbemdatetime_getvardate
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
 - SWbemDateTime.GetVarDate
 - ISWbemDateTime.GetVarDate
 - ISWbemDateTime.GetVarDate
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemDateTime::GetVarDate


## -description


The 
<b>GetVarDate</b> method of the 
<a href="https://msdn.microsoft.com/3dd34c73-3c2b-4d59-827b-169cf8020213">SWbemDateTime</a> object converts a date and time value in the CIM <a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">DATETIME</a> format to the <b>VT_DATE</b> format.

The <b>VT_DATE</b> format is an automation variant <a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">DATETIME</a> value that Visual Basic and ActiveX use.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param bIsLocal [in, optional]

Indicates whether  the returned value is interpreted as local time. The Coordinated Universal Time (UTC) property contains the local time converted to the correct UTC offset. If the value is <b>FALSE</b>, then the value is interpreted as UTC with a zero (0) offset.


### -param dVarDate






## -returns



The date and time value in the <b>VT_DATE</b> format.




## -remarks



<b>VT_DATE</b> and <b>FILETIME</b> values cannot contain wildcard fields.

The 
<b>GetVarDate</b> method fails (<b>wbemErrFailed</b>) if any of the following properties are <b>FALSE</b>:

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
 On successful return from 
<a href="https://msdn.microsoft.com/24c39d44-22ac-44ac-9e05-72a5b666ab19">SetVarDate</a>, all of these properties are set to <b>TRUE</b>.

After a successful call to 
<a href="https://msdn.microsoft.com/24c39d44-22ac-44ac-9e05-72a5b666ab19">SetVarDate</a>, the <a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">DATETIME</a> value is always interpreted as an absolute <b>DATETIME</b> value instead of an interval, 
and the <a href="https://msdn.microsoft.com/ba5fcf17-7c26-4960-9da9-e380d90e5f3e">IsInterval</a> is set to <b>FALSE</b>.

If 
<a href="https://msdn.microsoft.com/ba5fcf17-7c26-4960-9da9-e380d90e5f3e">IsInterval</a> is set to <b>TRUE</b>, then a call 
to <b>GetVarDate</b> results in the  <b>wbemErrFailed</b> error.

Some loss of precision occurs when you call  
<b>GetVarDate</b>, because <a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">datetime</a> values have a one microsecond  (μs) resolution, and <b>VT_DATE</b> values have a 500 millisecond resolution.


#### Examples

For examples of using the <a href="https://msdn.microsoft.com/3dd34c73-3c2b-4d59-827b-169cf8020213">SWbemDateTime</a>object to  convert CIM <a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">DATETIME</a> values to and from either the <b>FILETIME</b> or the <b>VT_DATE</b> format, see <a href="https://msdn.microsoft.com/dd01a732-5c88-4c24-a551-4d5452e712cc">WMI Tasks: Dates and Times</a>. For a description of the CIM <b>DATETIME</b> format, see <a href="https://msdn.microsoft.com/be239bf8-88a3-47bc-ae4f-49a5195e7a7d">Date and Time Format</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">DATETIME</a>



<a href="https://msdn.microsoft.com/3dd34c73-3c2b-4d59-827b-169cf8020213">SWbemDateTime</a>



<a href="https://msdn.microsoft.com/08e0761d-e735-454a-8429-2bd1eb331123">SWbemDateTime.GetFileTime</a>
 

 

