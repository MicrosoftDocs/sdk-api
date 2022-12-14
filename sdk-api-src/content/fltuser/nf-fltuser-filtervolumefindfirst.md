---
UID: NF:fltuser.FilterVolumeFindFirst
title: FilterVolumeFindFirst function (fltuser.h)
description: The FilterVolumeFindFirst function returns information about a volume.
helpviewer_keywords: ["FilterVolumeFindFirst","FilterVolumeFindFirst function [Installable File System Drivers]","FltWin32ApiRef_eb46c1c6-3137-4082-8272-8caccaeabf64.xml","fltuser/FilterVolumeFindFirst","ifsk.filtervolumefindfirst"]
old-location: ifsk\filtervolumefindfirst.htm
tech.root: ifsk
ms.assetid: c74ea261-bc9c-4fb0-a886-6947986566b2
ms.date: 12/05/2018
ms.keywords: FilterVolumeFindFirst, FilterVolumeFindFirst function [Installable File System Drivers], FltWin32ApiRef_eb46c1c6-3137-4082-8272-8caccaeabf64.xml, fltuser/FilterVolumeFindFirst, ifsk.filtervolumefindfirst
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
 - FilterVolumeFindFirst
 - fltuser/FilterVolumeFindFirst
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
 - FilterVolumeFindFirst
---

# FilterVolumeFindFirst function


## -description

The <b>FilterVolumeFindFirst</b> function returns information about a volume.

## -parameters

### -param dwInformationClass [in]

Type of requested information. This parameter can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
<b>FilterVolumeBasicInformation</b>

</td>
<td>
The buffer pointed to by the <i>lpBuffer</i> parameter receives a <a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_filter_volume_basic_information">FILTER_VOLUME_BASIC_INFORMATION</a> structure for the volume.

</td>
</tr>
<tr>
<td>
<b>FilterVolumeStandardInformation</b>

</td>
<td>
The buffer pointed to by the <i>lpBuffer</i> parameter receives a <a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_filter_volume_standard_information">FILTER_VOLUME_STANDARD_INFORMATION</a> structure for the volume. This structure is available starting with Windows Vista.

</td>
</tr>
</table>

### -param lpBuffer [out]

Pointer to a caller-allocated buffer that receives the requested information. The type of the information returned in the buffer is defined by the <i>dwInformationClass</i> parameter.

### -param dwBufferSize [in]

Size, in bytes, of the buffer that the <i>lpBuffer</i> parameter points to. The caller should set this parameter according to the given <i>dwInformationClass</i>.

### -param lpBytesReturned [out]

Pointer to a caller-allocated variable that receives the number of bytes returned in the buffer that <i>lpBuffer</i> points to if the call to <b>FilterVolumeFindFirst</b> succeeds. This parameter is required and cannot be <b>NULL</b>.

### -param lpVolumeFind [out]

Pointer to a caller-allocated variable that receives a search handle for the minifilter if the call to <b>FilterVolumeFindFirst</b> succeeds; otherwise, it receives INVALID_HANDLE_VALUE. This search handle can be used in subsequent calls to <a href="/windows/desktop/api/fltuser/nf-fltuser-filtervolumefindnext">FilterVolumeFindNext</a> and <a href="/windows/desktop/api/fltuser/nf-fltuser-filtervolumefindclose">FilterVolumeFindClose</a>.

## -returns

<b>FilterVolumeFindFirst</b> returns S_OK if it successfully returns information about a volume. Otherwise, it returns an HRESULT error value, such as one of the following:

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
An invalid value was specified for the <i>dwInformationClass</i> parameter.  For example, if <b>FilterVolumeStandardInformation</b> is specified for an operating system prior to Windows Vista, <b>FilterVolumeFindFirst</b> returns this HRESULT value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NO_MORE_ITEMS)</b></dt>
</dl>
</td>
<td width="60%">
A volume was not found in the list of volumes known to the filter manager.

</td>
</tr>
</table>

## -remarks

This <b>FilterVolumeFindFirst </b> function is used to begin scanning the volumes that are known to the filter manager.

<b>FilterVolumeFindFirst</b> opens a search handle and returns information about the first volume found in the list of volumes known to the filter manager. After the search handle has been established, use the <a href="/windows/desktop/api/fltuser/nf-fltuser-filtervolumefindnext">FilterVolumeFindNext</a> function to search for other volumes in the filter manager's list. When the search handle is no longer required, close it by calling <a href="/windows/desktop/api/fltuser/nf-fltuser-filtervolumefindclose">FilterVolumeFindClose</a>.

Note that when using <b>FilterVolumeFindFirst</b> and <a href="/windows/desktop/api/fltuser/nf-fltuser-filtervolumefindnext">FilterVolumeFindNext</a> to enumerate the list of volumes known to the filter manager, it is possible for two or more volumes in the list to have the same name.  For more information, see <a href="/windows-hardware/drivers/ifs/understanding-volume-enumerations-with-duplicate-volume-names">Understanding Volume Enumerations with Duplicate Volume Names</a>.

## -see-also

<a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_filter_volume_basic_information">FILTER_VOLUME_BASIC_INFORMATION</a>



<a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_filter_volume_standard_information">FILTER_VOLUME_STANDARD_INFORMATION</a>



<a href="/windows/desktop/api/fltuser/nf-fltuser-filtervolumefindclose">FilterVolumeFindClose</a>



<a href="/windows/desktop/api/fltuser/nf-fltuser-filtervolumefindnext">FilterVolumeFindNext</a>