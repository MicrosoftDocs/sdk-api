---
UID: NF:fltuser.FilterInstanceFindNext
title: FilterInstanceFindNext function
author: windows-sdk-content
description: The FilterInstanceFindNext function continues a minifilter driver instance search started by a call to FilterInstanceFindFirst.
old-location: ifsk\filterinstancefindnext.htm
old-project: ifsk
ms.assetid: c7305378-1de8-4db0-89a2-2ac342a17620
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: FilterInstanceFindNext, FilterInstanceFindNext function [Installable File System Drivers], FltWin32ApiRef_35023bec-f16b-4ac0-ad0f-f3550e8cfafd.xml, fltuser/FilterInstanceFindNext, ifsk.filterinstancefindnext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: fltuser.h
req.include-header: FltUser.h
req.redist: 
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FILTERED_DATA_SOURCES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - FltLib.dll
api_name:
 - FilterInstanceFindNext
product: Windows
targetos: Windows
req.lib: FltLib.lib
req.dll: FltLib.dll
req.irql: 
req.product: Internet Explorer 5
---

# FilterInstanceFindNext function


## -description


The <b>FilterInstanceFindNext</b> function continues a minifilter driver instance search started by a call to <a href="https://msdn.microsoft.com/4d397383-eb65-4646-80cd-203495513285">FilterInstanceFindFirst</a>. 


## -parameters




### -param hFilterInstanceFind [in]

Minifilter instance search handle returned by a previous call to <a href="https://msdn.microsoft.com/4d397383-eb65-4646-80cd-203495513285">FilterInstanceFindFirst</a>. 


### -param dwInformationClass [in]

The type of instance information structure returned.  This parameter must contain one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
<b>InstanceBasicInformation</b>

</td>
<td>
Return an <a href="https://msdn.microsoft.com/35e2b098-1bc2-4ffc-86c8-b60b651df027">INSTANCE_BASIC_INFORMATION</a> structure for the instance. 

</td>
</tr>
<tr>
<td>
<b>InstanceFullInformation</b>

</td>
<td>
Return an <a href="https://msdn.microsoft.com/6c034749-c110-4623-8a7b-a19235cad298">INSTANCE_FULL_INFORMATION</a> structure for the instance. 

</td>
</tr>
<tr>
<td>
<b>InstancePartialInformation</b>

</td>
<td>
Return an <a href="https://msdn.microsoft.com/cabcb39c-1f8d-41dc-a6ec-78f3fb3911cf">INSTANCE_PARTIAL_INFORMATION</a> structure for the instance. 

</td>
</tr>
<tr>
<td>
<b>InstanceAggregateStandardInformation</b>

</td>
<td>
Return an <a href="https://msdn.microsoft.com/35311ee7-d023-4b04-b510-a949ab9a40ca">INSTANCE_AGGREGATE_STANDARD_INFORMATION</a> structure for the instance.  The LegacyFilter portion of the structure is not utilized.  This structure is available starting with Windows Vista.

</td>
</tr>
</table>
 


### -param lpBuffer [out]

Pointer to a caller-allocated buffer that receives the requested information. The type of the information returned in the buffer is defined by the <i>dwInformationClass</i> parameter.


### -param dwBufferSize [in]

Size, in bytes, of the buffer that the <i>lpBuffer</i> parameter points to. The caller should set this parameter according to the given <i>dwInformationClass</i>.


### -param lpBytesReturned [out]

Pointer to a caller-allocated variable that receives the number of bytes returned in the buffer that <i>lpBuffer</i> points to if the call to <b>FilterInstanceFindNext</b> succeeds. This parameter is required and cannot be <b>NULL</b>.


## -returns



<b>FilterInstanceFindNext</b> returns S_OK if successful. Otherwise, it returns an HRESULT error value, such as one of the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)</b></dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by <i>lpBuffer</i> is not large enough to contain the requested information.  When this value is returned, <i>lpBytesReturned</i> will contain the size, in bytes, of the buffer required for the given <i>dwInformationClass</i> structure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_PARAMETER)</b></dt>
</dl>
</td>
<td width="60%">
An invalid value was specified for the <i>dwInformationClass</i> parameter.  For example, if <b>InstanceAggregateStandardInformation</b> is specified for an operating system prior to Windows Vista, <b>FilterInstanceFindNext</b> returns this HRESULT value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NO_MORE_ITEMS)</b></dt>
</dl>
</td>
<td width="60%">
This HRESULT value is returned if there are no more unique instances of the minifilter.

</td>
</tr>
</table>
 




## -remarks



After the search handle is established by calling <a href="https://msdn.microsoft.com/4d397383-eb65-4646-80cd-203495513285">FilterInstanceFindFirst</a>, call <b>FilterInstanceFindNext</b> to search for other instances for the minifilter specified in the call to <b>FilterInstanceFindFirst</b>. 

<b>FilterInstanceFindNext</b> finds one instance per call. 




## -see-also




<a href="https://msdn.microsoft.com/f4b066ca-4154-425d-85f6-682dc7460117">FilterInstanceFindClose</a>



<a href="https://msdn.microsoft.com/4d397383-eb65-4646-80cd-203495513285">FilterInstanceFindFirst</a>



<a href="https://msdn.microsoft.com/35311ee7-d023-4b04-b510-a949ab9a40ca">INSTANCE_AGGREGATE_STANDARD_INFORMATION</a>



<a href="https://msdn.microsoft.com/35e2b098-1bc2-4ffc-86c8-b60b651df027">INSTANCE_BASIC_INFORMATION</a>



<a href="https://msdn.microsoft.com/6c034749-c110-4623-8a7b-a19235cad298">INSTANCE_FULL_INFORMATION</a>



<a href="https://msdn.microsoft.com/cabcb39c-1f8d-41dc-a6ec-78f3fb3911cf">INSTANCE_PARTIAL_INFORMATION</a>
 

 

