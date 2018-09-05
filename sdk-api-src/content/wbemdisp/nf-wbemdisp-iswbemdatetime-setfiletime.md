---
UID: NF:wbemdisp.ISWbemDateTime.SetFileTime
title: ISWbemDateTime::SetFileTime
author: windows-sdk-content
description: Converts a date in the string FILETIME format to the CIM datetime format.
old-location: wmi\swbemdatetime_setfiletime.htm
old-project: WmiSdk
ms.assetid: e375afda-5e94-46d6-b1ac-e801e0f4a620
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: ISWbemDateTime interface [Windows Management Instrumentation],SetFileTime method, ISWbemDateTime.SetFileTime, ISWbemDateTime::SetFileTime, SWbemDateTime object [Windows Management Instrumentation],SetFileTime method, SWbemDateTime.SetFileTime, SetFileTime, SetFileTime method [Windows Management Instrumentation], SetFileTime method [Windows Management Instrumentation],ISWbemDateTime interface, SetFileTime method [Windows Management Instrumentation],SWbemDateTime object, _hmm_swbemdatetime.setfiletime, wmi.swbemdatetime_setfiletime
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
 - SWbemDateTime.SetFileTime
 - ISWbemDateTime.SetFileTime
 - ISWbemDateTime.SetFileTime
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemDateTime::SetFileTime


## -description


The 
<b>SetFileTime</b> method of the 
<a href="https://msdn.microsoft.com/3dd34c73-3c2b-4d59-827b-169cf8020213">SWbemDateTime</a> object converts a date in the string <b>FILETIME</b> format to the <a href="https://msdn.microsoft.com/be239bf8-88a3-47bc-ae4f-49a5195e7a7d">CIM datetime</a> format.

The <b>FILETIME</b> format is a 64-bit datetime structure that  represents the number of 100-nanosecond units since the beginning of January 1, 1601.
Windows Management Instrumentation (WMI) treats <b>FILETIME</b> values as string representations of unsigned 64-bit numbers.

For the syntax explanation, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param strFileTime [in]

<b>FILETIME</b> value used to set the object.


### -param bIsLocal [in, optional]

If <b>TRUE</b>, <i>strFileTime</i> is interpreted as a local time. The Coordinated Universal Time (UTC) property contains the local time converted to the correct UTC offset. When <i>bIsLocal</i> is <b>FALSE</b>, then <i>strFileTime</i> is converted directly into a UTC value with an offset of 0 (zero).


## -returns



This method does not return a value.




## -remarks



After a successful call to 
<b>SetFileTime</b>, the <a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">datetime</a> value is always interpreted as an absolute (<b>datetime</b>) value, and <a href="https://msdn.microsoft.com/ba5fcf17-7c26-4960-9da9-e380d90e5f3e">IsInterval</a> is set to <b>FALSE</b>.


#### Examples

For examples of using the <a href="https://msdn.microsoft.com/3dd34c73-3c2b-4d59-827b-169cf8020213">SWbemDateTime</a>object to convert CIM <a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">DATETIME</a> values to and from either the <b>FILETIME</b> format or the <b>VT_DATE</b> format, see <a href="https://msdn.microsoft.com/dd01a732-5c88-4c24-a551-4d5452e712cc">WMI Tasks: Dates and Times</a>. For a description of the CIM <b>DATETIME</b> format, see <a href="https://msdn.microsoft.com/be239bf8-88a3-47bc-ae4f-49a5195e7a7d">Date and Time Format</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">DATETIME</a>



<a href="https://msdn.microsoft.com/3dd34c73-3c2b-4d59-827b-169cf8020213">SWbemDateTime</a>



<a href="https://msdn.microsoft.com/24c39d44-22ac-44ac-9e05-72a5b666ab19">SWbemDateTime.SetVarDate</a>
 

 

