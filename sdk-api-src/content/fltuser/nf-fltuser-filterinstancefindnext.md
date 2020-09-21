---
UID: NF:fltuser.FilterInstanceFindNext
title: FilterInstanceFindNext function (fltuser.h)
description: The FilterInstanceFindNext function continues a minifilter driver instance search started by a call to FilterInstanceFindFirst.
helpviewer_keywords: ["FilterInstanceFindNext","FilterInstanceFindNext function [Installable File System Drivers]","FltWin32ApiRef_35023bec-f16b-4ac0-ad0f-f3550e8cfafd.xml","fltuser/FilterInstanceFindNext","ifsk.filterinstancefindnext"]
old-location: ifsk\filterinstancefindnext.htm
tech.root: ifsk
ms.assetid: c7305378-1de8-4db0-89a2-2ac342a17620
ms.date: 12/05/2018
ms.keywords: FilterInstanceFindNext, FilterInstanceFindNext function [Installable File System Drivers], FltWin32ApiRef_35023bec-f16b-4ac0-ad0f-f3550e8cfafd.xml, fltuser/FilterInstanceFindNext, ifsk.filterinstancefindnext
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
 - FilterInstanceFindNext
 - fltuser/FilterInstanceFindNext
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
 - FilterInstanceFindNext
---

# FilterInstanceFindNext function


## -description

The <b>FilterInstanceFindNext</b> function continues a minifilter driver instance search started by a call to <a href="/windows/desktop/api/fltuser/nf-fltuser-filterinstancefindfirst">FilterInstanceFindFirst</a>.

## -parameters

### -param hFilterInstanceFind [in]

Minifilter instance search handle returned by a previous call to <a href="/windows/desktop/api/fltuser/nf-fltuser-filterinstancefindfirst">FilterInstanceFindFirst</a>.

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

After the search handle is established by calling <a href="/windows/desktop/api/fltuser/nf-fltuser-filterinstancefindfirst">FilterInstanceFindFirst</a>, call <b>FilterInstanceFindNext</b> to search for other instances for the minifilter specified in the call to <b>FilterInstanceFindFirst</b>. 

<b>FilterInstanceFindNext</b> finds one instance per call.

## -see-also

<a href="/windows/desktop/api/fltuser/nf-fltuser-filterinstancefindclose">FilterInstanceFindClose</a>



<a href="/windows/desktop/api/fltuser/nf-fltuser-filterinstancefindfirst">FilterInstanceFindFirst</a>



<a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_instance_aggregate_standard_information">INSTANCE_AGGREGATE_STANDARD_INFORMATION</a>



<a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_instance_basic_information">INSTANCE_BASIC_INFORMATION</a>



<a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_instance_full_information">INSTANCE_FULL_INFORMATION</a>



<a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_instance_partial_information">INSTANCE_PARTIAL_INFORMATION</a>