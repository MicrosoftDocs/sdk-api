---
UID: NF:evntprov.EventSetInformation
title: EventSetInformation function (evntprov.h)
description: Performs operations on a registration object.
old-location: etw\eventsetinformation.htm
tech.root: ETW
ms.assetid: e8b408ba-4bb5-4166-bf43-d18e4fe8de32
ms.date: 12/05/2018
ms.keywords: EventSetInformation, EventSetInformation function [ETW], etw.eventsetinformation, evntprov/EventSetInformation
f1_keywords:
- evntprov/EventSetInformation
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EventSetInformation function


## -description


Performs operations on a registration
    object.


## -parameters




### -param RegHandle [in]

Type: <b>REGHANDLE</b>

Registration handle returned by 
      <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/nf-evntprov-eventregister">EventRegister</a>.


### -param InformationClass [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/evntprov/ne-evntprov-event_info_class">EVENT_INFO_CLASS</a></b>

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
Use <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string 
        for the returned error.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/evntprov/ne-evntprov-event_info_class">EVENT_INFO_CLASS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/evntprov/nf-evntprov-eventregister">EventRegister</a>
 

 

