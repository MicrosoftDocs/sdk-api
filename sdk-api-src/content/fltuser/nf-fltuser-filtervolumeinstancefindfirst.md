---
UID: NF:fltuser.FilterVolumeInstanceFindFirst
title: FilterVolumeInstanceFindFirst function (fltuser.h)
description: The FilterVolumeInstanceFindFirst function returns information about a minifilter driver instance or legacy filter driver and is used to begin scanning the filter drivers that are attached to a volume.
helpviewer_keywords: ["FilterVolumeInstanceFindFirst","FilterVolumeInstanceFindFirst function [Installable File System Drivers]","FltWin32ApiRef_3a784a96-c717-4118-bf97-bba9ac4b7736.xml","fltuser/FilterVolumeInstanceFindFirst","ifsk.filtervolumeinstancefindfirst"]
old-location: ifsk\filtervolumeinstancefindfirst.htm
tech.root: ifsk
ms.assetid: 8bcaa20e-90f8-4e18-88b0-85a6b6632ef7
ms.date: 12/05/2018
ms.keywords: FilterVolumeInstanceFindFirst, FilterVolumeInstanceFindFirst function [Installable File System Drivers], FltWin32ApiRef_3a784a96-c717-4118-bf97-bba9ac4b7736.xml, fltuser/FilterVolumeInstanceFindFirst, ifsk.filtervolumeinstancefindfirst
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
 - FilterVolumeInstanceFindFirst
 - fltuser/FilterVolumeInstanceFindFirst
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
 - FilterVolumeInstanceFindFirst
---

# FilterVolumeInstanceFindFirst function


## -description

The <b>FilterVolumeInstanceFindFirst</b> function returns information about a minifilter driver instance or legacy filter driver and is used to begin scanning the filter drivers that are attached to a volume.

## -parameters

### -param lpVolumeName [in]

Pointer to a null-terminated wide-character string that contains the name of the volume to which the minifilter instance or legacy filter is attached.

The <i>lpVolumeName</i> input string can be any of the following. The trailing backslash (\\) is optional. 

<ul>
<li>
 A drive letter, such as D:\

</li>
<li>
 A path to a volume mount point, such as c:\mnt\edrive\

</li>
<li>
 A unique volume identifier (also called a <i>volume GUID name</i>), such as \??\Volume{7603f260-142a-11d4-ac67-806d6172696f}\

</li>
<li>
 A nonpersistent device name (also called a <i>target name</i> or an <i>NT device name</i>), such as \Device\HarddiskVolume1\

</li>
</ul>

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

Pointer to a caller-allocated variable that receives the number of bytes returned in the buffer that <i>lpBuffer</i> points to if the call to <b>FilterVolumeInstanceFindFirst</b> succeeds. This parameter is required and cannot be <b>NULL</b>.

### -param lpVolumeInstanceFind [out]

Pointer to a caller-allocated variable that receives a search handle for the minifilter instance or legacy filter (only when <b>InstanceAggregateStandardInformation</b> is specified) if the call to <b>FilterVolumeInstanceFindFirst</b> succeeds. Otherwise, <i>lpVolumeInstanceFind</i> receives INVALID_HANDLE_VALUE. This search handle can be used in subsequent calls to <a href="/windows/desktop/api/fltuser/nf-fltuser-filtervolumeinstancefindnext">FilterVolumeInstanceFindNext</a> and <a href="/windows/desktop/api/fltuser/nf-fltuser-filtervolumeinstancefindclose">FilterVolumeInstanceFindClose</a>.

## -returns

<b>FilterVolumeInstanceFindFirst</b> returns S_OK if successful. Otherwise, it returns an HRESULT error value, such as one of the following:

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
An invalid value was specified for the <i>dwInformationClass</i> parameter.  For example, if <b>InstanceAggregateStandardInformation</b> is specified for an operating system prior to Windows Vista, <b>FilterVolumeInstanceFindFirst</b> returns this HRESULT value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NO_MORE_ITEMS)</b></dt>
</dl>
</td>
<td width="60%">
A filter driver was not found on the given volume.

</td>
</tr>
</table>

## -remarks

The <b>FilterVolumeInstanceFindFirst</b> function opens a search handle and returns information about the first filter driver found that is attached to the volume named by <i>lpVolumeName</i>. After the search handle has been established, call <a href="/windows/desktop/api/fltuser/nf-fltuser-filtervolumeinstancefindnext">FilterVolumeInstanceFindNext</a> to search for other filter drivers that are attached to the same volume. When the search handle is no longer needed, close it by calling <a href="/windows/desktop/api/fltuser/nf-fltuser-filtervolumeinstancefindclose">FilterVolumeInstanceFindClose</a>. 

Starting with Windows Vista, <b>FilterVolumeInstanceFindFirst</b> can return both legacy filter driver information and minifilter driver instance information when the value of the <i>dwInformationClass</i> parameter is <b>InstanceAggregateStandardInformation</b>.  For earlier operating systems, this function cannot return legacy filter information because the INSTANCE_AGGREGATE_STANDARD_INFORMATION structure is not available.

## -see-also

<a href="/windows/desktop/api/fltuser/nf-fltuser-filtervolumeinstancefindclose">FilterVolumeInstanceFindClose</a>



<a href="/windows/desktop/api/fltuser/nf-fltuser-filtervolumeinstancefindnext">FilterVolumeInstanceFindNext</a>



<a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_instance_aggregate_standard_information">INSTANCE_AGGREGATE_STANDARD_INFORMATION</a>



<a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_instance_basic_information">INSTANCE_BASIC_INFORMATION</a>



<a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_instance_full_information">INSTANCE_FULL_INFORMATION</a>



<a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_instance_partial_information">INSTANCE_PARTIAL_INFORMATION</a>