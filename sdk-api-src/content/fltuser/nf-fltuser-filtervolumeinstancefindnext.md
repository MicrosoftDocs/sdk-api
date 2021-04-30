---
UID: NF:fltuser.FilterVolumeInstanceFindNext
title: FilterVolumeInstanceFindNext function (fltuser.h)
description: The FilterVolumeInstanceFindNext function continues a minifilter driver instance or legacy filter driver search started by a call to FilterVolumeInstanceFindFirst.
helpviewer_keywords: ["FilterVolumeInstanceFindNext","FilterVolumeInstanceFindNext function [Installable File System Drivers]","FltWin32ApiRef_646e3187-31a8-42fb-b8a6-bca598605660.xml","fltuser/FilterVolumeInstanceFindNext","ifsk.filtervolumeinstancefindnext"]
old-location: ifsk\filtervolumeinstancefindnext.htm
tech.root: ifsk
ms.assetid: e4bcd797-5a1a-45b9-a4f2-387ea1df7c2f
ms.date: 12/05/2018
ms.keywords: FilterVolumeInstanceFindNext, FilterVolumeInstanceFindNext function [Installable File System Drivers], FltWin32ApiRef_646e3187-31a8-42fb-b8a6-bca598605660.xml, fltuser/FilterVolumeInstanceFindNext, ifsk.filtervolumeinstancefindnext
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
 - FilterVolumeInstanceFindNext
 - fltuser/FilterVolumeInstanceFindNext
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
 - FilterVolumeInstanceFindNext
---

# FilterVolumeInstanceFindNext function


## -description

The <b>FilterVolumeInstanceFindNext</b> function continues a minifilter driver instance or legacy filter driver search started by a call to <a href="/windows/desktop/api/fltuser/nf-fltuser-filtervolumeinstancefindfirst">FilterVolumeInstanceFindFirst</a>.

## -parameters

### -param hVolumeInstanceFind [in]

Volume filter driver search handle returned by a previous call to <a href="/windows/desktop/api/fltuser/nf-fltuser-filtervolumeinstancefindfirst">FilterVolumeInstanceFindFirst</a>.

### -param dwInformationClass [in]

The type of filter driver information structure returned.  This parameter must contain one of the following values.

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
Return an <a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_instance_basic_information">INSTANCE_BASIC_INFORMATION</a> structure for a minifilter instance.  Legacy filter drivers are ignored.

</td>
</tr>
<tr>
<td>
<b>InstanceFullInformation</b>

</td>
<td>
Return an <a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_instance_full_information">INSTANCE_FULL_INFORMATION</a> structure for a minifilter instance.  Legacy filter drivers are ignored.

</td>
</tr>
<tr>
<td>
<b>InstancePartialInformation</b>

</td>
<td>
Return an <a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_instance_partial_information">INSTANCE_PARTIAL_INFORMATION</a> structure for a minifilter instance.  Legacy filter drivers are ignored.

</td>
</tr>
<tr>
<td>
<b>InstanceAggregateStandardInformation</b>

</td>
<td>
Return an <a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_instance_aggregate_standard_information">INSTANCE_AGGREGATE_STANDARD_INFORMATION</a> structure for the instance. The <b>LegacyFilter</b> member of the structure is not utilized. 

This structure is available starting with Windows Vista.

</td>
</tr>
</table>

### -param lpBuffer [out]

Pointer to a caller-allocated buffer that receives the requested information. The type of the information returned in the buffer is defined by the <i>dwInformationClass</i> parameter.

### -param dwBufferSize [in]

Size, in bytes, of the buffer that the <i>lpBuffer</i> parameter points to. The caller should set this parameter according to the given <i>dwInformationClass</i>.

### -param lpBytesReturned [out]

Pointer to a caller-allocated variable that receives the number of bytes returned in the buffer that <i>lpBuffer</i> points to if the call to <b>FilterVolumeInstanceFindNext</b> succeeds. This parameter is required and cannot be <b>NULL</b>.

## -returns

<b>FilterVolumeInstanceFindNext</b> returns S_OK if successful. Otherwise, it returns an HRESULT error value, such as one of the following:

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
An invalid value was specified for the <i>dwInformationClass</i> parameter.  For example, if <b>InstanceAggregateStandardInformation</b> is specified for an operating system prior to Windows Vista, <b>FilterVolumeInstanceFindNext</b> returns this HRESULT value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NO_MORE_ITEMS)</b></dt>
</dl>
</td>
<td width="60%">
No more filter drivers were found on the given volume.

</td>
</tr>
</table>

## -remarks

<b>FilterVolumeInstanceFindNext</b> finds one filter driver per call.

After the search handle is established by calling <b>FilterVolumeInstanceFindFirst</b>, use the <b>FilterVolumeInstanceFindNext</b> function to search for other filter drivers that are attached to the volume specified in the call to <a href="/windows/desktop/api/fltuser/nf-fltuser-filtervolumeinstancefindfirst">FilterVolumeInstanceFindFirst</a>. When the search handle is no longer required, close it by calling <a href="/windows/desktop/api/fltuser/nf-fltuser-filtervolumeinstancefindclose">FilterVolumeInstanceFindClose</a>.

Starting with Windows Vista, this routine can return both legacy filter driver information and minifilter driver instance information when the value of the <i>dwInformationClass</i> parameter is <b>InstanceAggregateStandardInformation</b>.  For earlier operating systems, this routine cannot return legacy filter information because the INSTANCE_AGGREGATE_STANDARD_INFORMATION structure is not available.

## -see-also

<a href="/windows/desktop/api/fltuser/nf-fltuser-filtervolumeinstancefindclose">FilterVolumeInstanceFindClose</a>



<a href="/windows/desktop/api/fltuser/nf-fltuser-filtervolumeinstancefindfirst">FilterVolumeInstanceFindFirst</a>



<a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_instance_aggregate_standard_information">INSTANCE_AGGREGATE_STANDARD_INFORMATION</a>



<a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_instance_basic_information">INSTANCE_BASIC_INFORMATION</a>



<a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_instance_full_information">INSTANCE_FULL_INFORMATION</a>



<a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_instance_partial_information">INSTANCE_PARTIAL_INFORMATION</a>