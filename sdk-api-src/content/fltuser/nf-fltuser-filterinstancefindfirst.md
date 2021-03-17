---
UID: NF:fltuser.FilterInstanceFindFirst
title: FilterInstanceFindFirst function (fltuser.h)
description: The FilterInstanceFindFirst function returns information about a minifilter driver instance and is used as a starting point for scanning the instances of a minifilter.
helpviewer_keywords: ["FilterInstanceFindFirst","FilterInstanceFindFirst function [Installable File System Drivers]","FltWin32ApiRef_c49ec801-8b52-42c5-9495-7fd4eb999480.xml","fltuser/FilterInstanceFindFirst","ifsk.filterinstancefindfirst"]
old-location: ifsk\filterinstancefindfirst.htm
tech.root: ifsk
ms.assetid: 4d397383-eb65-4646-80cd-203495513285
ms.date: 12/05/2018
ms.keywords: FilterInstanceFindFirst, FilterInstanceFindFirst function [Installable File System Drivers], FltWin32ApiRef_c49ec801-8b52-42c5-9495-7fd4eb999480.xml, fltuser/FilterInstanceFindFirst, ifsk.filterinstancefindfirst
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
req.lib: FltLib.lib
req.dll: FltLib.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FilterInstanceFindFirst
 - fltuser/FilterInstanceFindFirst
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - FltLib.dll
api_name:
 - FilterInstanceFindFirst
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
Return an <a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_instance_basic_information">INSTANCE_BASIC_INFORMATION</a> structure for the instance. 

</td>
</tr>
<tr>
<td>
<b>InstanceFullInformation</b>

</td>
<td>
Return an <a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_instance_full_information">INSTANCE_FULL_INFORMATION</a> structure for the instance. 

</td>
</tr>
<tr>
<td>
<b>InstancePartialInformation</b>

</td>
<td>
Return an <a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_instance_partial_information">INSTANCE_PARTIAL_INFORMATION</a> structure for the instance. 

</td>
</tr>
<tr>
<td>
<b>InstanceAggregateStandardInformation</b>

</td>
<td>
Return an <a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_instance_aggregate_standard_information">INSTANCE_AGGREGATE_STANDARD_INFORMATION</a> structure for the instance.  The LegacyFilter portion of the structure is not utilized.  This structure is available starting with Windows Vista.

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

Pointer to a caller-allocated variable that receives a search handle for the minifilter if the call to <b>FilterInstanceFindFirst</b> succeeds; otherwise, it receives INVALID_HANDLE_VALUE. This search handle can be used in subsequent calls to <a href="/windows/desktop/api/fltuser/nf-fltuser-filterinstancefindnext">FilterInstanceFindNext</a> and <a href="/windows/desktop/api/fltuser/nf-fltuser-filterinstancefindclose">FilterInstanceFindClose</a>.

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

The <b>FilterInstanceFindFirst</b> function opens a search handle and returns information about an instance for the minifilter named by <i>lpFilterName</i>. After the search handle has been established, call <a href="/windows/desktop/api/fltuser/nf-fltuser-filterinstancefindnext">FilterInstanceFindNext</a> to search for other instances of the same minifilter. When the search handle is no longer needed, close it by calling <a href="/windows/desktop/api/fltuser/nf-fltuser-filterinstancefindclose">FilterInstanceFindClose</a>.

## -see-also

<a href="/windows/desktop/api/fltuser/nf-fltuser-filterinstancefindclose">FilterInstanceFindClose</a>



<a href="/windows/desktop/api/fltuser/nf-fltuser-filterinstancefindnext">FilterInstanceFindNext</a>



<a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_instance_aggregate_standard_information">INSTANCE_AGGREGATE_STANDARD_INFORMATION</a>



<a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_instance_basic_information">INSTANCE_BASIC_INFORMATION</a>



<a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_instance_full_information">INSTANCE_FULL_INFORMATION</a>



<a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_instance_partial_information">INSTANCE_PARTIAL_INFORMATION</a>