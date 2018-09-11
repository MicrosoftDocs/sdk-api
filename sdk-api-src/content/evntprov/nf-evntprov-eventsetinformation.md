---
UID: NF:evntprov.EventSetInformation
title: EventSetInformation function
author: windows-sdk-content
description: Performs operations on a registration object.
old-location: etw\eventsetinformation.htm
tech.root: etw
ms.assetid: e8b408ba-4bb5-4166-bf43-d18e4fe8de32
ms.author: windowssdkdev
ms.date: 08/08/2018
ms.keywords: EventSetInformation, EventSetInformation function [ETW], etw.eventsetinformation, evntprov/EventSetInformation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: evntprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-eventing-provider-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Eventing-Provider-L1-1-1.dll
api_name:
 - EventSetInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EventSetInformation function


## -description


Performs operations on a registration
    object.


## -parameters




### -param RegHandle [in]

Type: <b>REGHANDLE</b>

Registration handle returned by 
      <a href="https://msdn.microsoft.com/6025c3a6-7d88-49dc-bbc3-655c172dde3c">EventRegister</a>.


### -param InformationClass [in]

Type: <b><a href="https://msdn.microsoft.com/76ac2b93-d5df-4504-b36d-1530bbb12ab4">EVENT_INFO_CLASS</a></b>

Type of operation to be performed on the registration object.


### -param EventInformation [in]

Type: <b>PVOID</b>

The input buffer.


### -param InformationLength [in]

Type: <b>ULONG</b>

Size of the input buffer.


## -returns



Type: <b>ULONG</b>

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The parameter is incorrect. This error is returned if the <i>RegHandle</i> parameter 
        is not a valid registration handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Use <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string 
        for the returned error.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/76ac2b93-d5df-4504-b36d-1530bbb12ab4">EVENT_INFO_CLASS</a>



<a href="https://msdn.microsoft.com/6025c3a6-7d88-49dc-bbc3-655c172dde3c">EventRegister</a>
 

 

