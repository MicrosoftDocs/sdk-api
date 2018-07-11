---
UID: NF:fltuser.FilterInstanceFindFirst
title: FilterInstanceFindFirst function
author: windows-sdk-content
description: The FilterInstanceFindFirst function returns information about a minifilter driver instance and is used as a starting point for scanning the instances of a minifilter.
old-location: ifsk\filterinstancefindfirst.htm
old-project: ifsk
ms.assetid: 4d397383-eb65-4646-80cd-203495513285
ms.author: windowssdkdev
ms.date: 04/17/2018
ms.keywords: FilterInstanceFindFirst, FilterInstanceFindFirst function [Installable File System Drivers], FltWin32ApiRef_c49ec801-8b52-42c5-9495-7fd4eb999480.xml, fltuser/FilterInstanceFindFirst, ifsk.filterinstancefindfirst
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: fltuser.h
req.include-header: FltUser.h
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
 - FilterInstanceFindFirst
product: Windows
targetos: Windows
req.lib: FltLib.lib
req.dll: FltLib.dll
req.irql: 
req.product: Internet Explorer 5
---

# FilterInstanceFindFirst function


## -description


The <b>FilterInstanceFindFirst</b> function returns information about a minifilter driver instance and is used as a starting point for scanning the instances of a minifilter. 


## -parameters




### -param lpFilterName [in]

Pointer to a null-terminated wide-character string that contains the name of the minifilter driver that owns the instance. 


### -param dwInformationClass [in]

The type of instance information structure returned.  This parameter must be one of the following values.

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
Return an <a href="https://msdn.microsoft.com/library/windows/hardware/ff548176">INSTANCE_BASIC_INFORMATION</a> structure for the instance. 

</td>
</tr>
<tr>
<td>
<b>InstanceFullInformation</b>

</td>
<td>
Return an <a href="https://msdn.microsoft.com/library/windows/hardware/ff548185">INSTANCE_FULL_INFORMATION</a> structure for the instance. 

</td>
</tr>
<tr>
<td>
<b>InstancePartialInformation</b>

</td>
<td>
Return an <a href="https://msdn.microsoft.com/library/windows/hardware/ff548190">INSTANCE_PARTIAL_INFORMATION</a> structure for the instance. 

</td>
</tr>
<tr>
<td>
<b>InstanceAggregateStandardInformation</b>

</td>
<td>
Return an <a href="https://msdn.microsoft.com/library/windows/hardware/ff548172">INSTANCE_AGGREGATE_STANDARD_INFORMATION</a> structure for the instance.  The LegacyFilter portion of the structure is not utilized.  This structure is available starting with Windows Vista.

</td>
</tr>
</table>
 


### -param lpBuffer [out]

Pointer to a caller-allocated buffer that receives the requested information. The type of the information returned in the buffer is defined by the <i>dwInformationClass</i> parameter. 


### -param dwBufferSize [in]

Size, in bytes, of the buffer that the <i>lpBuffer</i> parameter points to. The caller should set this parameter according to the given <i>dwInformationClass</i>. 


### -param lpBytesReturned [out]

Pointer to a caller-allocated variable that receives the number of bytes returned in the buffer that <i>lpBuffer</i> points to, if the call to <b>FilterInstanceFindFirst</b> succeeds. This parameter is required and cannot be <b>NULL</b>. 


### -param lpFilterInstanceFind [out]

Pointer to a caller-allocated variable that receives a search handle for the minifilter if the call to <b>FilterInstanceFindFirst</b> succeeds; otherwise, it receives INVALID_HANDLE_VALUE. This search handle can be used in subsequent calls to <a href="https://msdn.microsoft.com/library/windows/hardware/ff541493">FilterInstanceFindNext</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff540538">FilterInstanceFindClose</a>. 


## -returns



<b>FilterInstanceFindFirst</b> returns S_OK if successful. Otherwise, it returns an HRESULT error value, such as one of the following:

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
An invalid value was specified for the <i>dwInformationClass</i> parameter.  For example, if <b>InstanceAggregateStandardInformation</b> is specified for operating systems prior to Windows Vista, the function returns this HRESULT value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NO_MORE_ITEMS)</b></dt>
</dl>
</td>
<td width="60%">
The minifilter specified by the <i>lpFilterName</i> parameter does not have an instance on the file system stack.

</td>
</tr>
</table>
 




## -remarks



The <b>FilterInstanceFindFirst</b> function opens a search handle and returns information about an instance for the minifilter named by <i>lpFilterName</i>. After the search handle has been established, call <a href="https://msdn.microsoft.com/library/windows/hardware/ff541493">FilterInstanceFindNext</a> to search for other instances of the same minifilter. When the search handle is no longer needed, close it by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff540538">FilterInstanceFindClose</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff540538">FilterInstanceFindClose</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541493">FilterInstanceFindNext</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff548172">INSTANCE_AGGREGATE_STANDARD_INFORMATION</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff548176">INSTANCE_BASIC_INFORMATION</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff548185">INSTANCE_FULL_INFORMATION</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff548190">INSTANCE_PARTIAL_INFORMATION</a>
 

 

