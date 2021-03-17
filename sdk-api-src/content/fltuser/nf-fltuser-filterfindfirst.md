---
UID: NF:fltuser.FilterFindFirst
title: FilterFindFirst function (fltuser.h)
description: The FilterFindFirst function returns information about a filter driver (minifilter driver instance or legacy filter driver) and is used to begin scanning the filters in the global list of registered filters.
helpviewer_keywords: ["FilterFindFirst","FilterFindFirst function [Installable File System Drivers]","FltWin32ApiRef_1e28a34d-5d84-42cb-b530-24cac8c7b4dc.xml","fltuser/FilterFindFirst","ifsk.filterfindfirst"]
old-location: ifsk\filterfindfirst.htm
tech.root: ifsk
ms.assetid: e6a7c5a2-838d-47b1-ab16-aa1d27806f53
ms.date: 12/05/2018
ms.keywords: FilterFindFirst, FilterFindFirst function [Installable File System Drivers], FltWin32ApiRef_1e28a34d-5d84-42cb-b530-24cac8c7b4dc.xml, fltuser/FilterFindFirst, ifsk.filterfindfirst
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
 - FilterFindFirst
 - fltuser/FilterFindFirst
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
 - FilterFindFirst
---

# FilterFindFirst function


## -description

The <b>FilterFindFirst</b> function returns information about a filter driver (minifilter driver instance or legacy filter driver) and is used to begin scanning the filters in the global list of registered filters.

## -parameters

### -param dwInformationClass [in]

Type of filter driver information requested. This parameter must be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
<b>FilterFullInformation</b>

</td>
<td>
The buffer pointed to by the <i>lpBuffer</i> parameter receives a <a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_filter_full_information">FILTER_FULL_INFORMATION</a> structure for each minifilter instance. Legacy filters are ignored.

</td>
</tr>
<tr>
<td>
<b>FilterAggregateBasicInformation</b>

</td>
<td>
The buffer pointed to by the <i>lpBuffer</i> parameter receives a <a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_filter_aggregate_basic_information">FILTER_AGGREGATE_BASIC_INFORMATION</a> structure for each minifilter instance or legacy filter. This <i>dwInformationClass</i> value is available starting with Windows Server 2003 with SP1 and Windows XP with SP2 with filter manager rollup.  For more information about the filter manager rollup package for Windows XP with SP2, see article 914882, " <a href="https://support.microsoft.com/?kbid&amp;ID=914882">The filter manager rollup package for Windows XP SP2</a>," in the Microsoft Knowledge Base.

</td>
</tr>
<tr>
<td>
<b>FilterAggregateStandardInformation</b>

</td>
<td>
The buffer pointed to by the <i>lpBuffer</i> parameter receives a <a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_filter_aggregate_standard_information">FILTER_AGGREGATE_STANDARD_INFORMATION</a> structure for each minifilter instance or legacy filter. This <i>dwInformationClass</i> value is available starting with Windows Vista.

</td>
</tr>
</table>

### -param lpBuffer [out]

Pointer to a caller-allocated buffer that receives the requested information. The type of the information returned in the buffer is defined by the <i>dwInformationClass</i> parameter.

### -param dwBufferSize [in]

Size, in bytes, of the buffer that the <i>lpBuffer</i> parameter points to. The caller should set this parameter according to the given <i>dwInformationClass</i>.

### -param lpBytesReturned [out]

Pointer to a caller-allocated variable that receives the number of bytes returned in the buffer that <i>lpBuffer</i> points to if the call to <b>FilterFindFirst</b> succeeds. This parameter is required and cannot be <b>NULL</b>.

### -param lpFilterFind [out]

Pointer to a caller-allocated variable that receives a search handle for the filter driver if the call to <b>FilterFindFirst</b> succeeds; otherwise, it receives INVALID_HANDLE_VALUE. This search handle can be used in subsequent calls to <a href="/windows/desktop/api/fltuser/nf-fltuser-filterfindnext">FilterFindNext</a> and <a href="/windows/desktop/api/fltuser/nf-fltuser-filterfindclose">FilterFindClose</a>.

## -returns

<b>FilterFindFirst</b> returns S_OK if successful. Otherwise, it returns an HRESULT error value, such as one of the following:

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
An invalid value was specified for the <i>dwInformationClass</i> parameter.  For example, if <i>FilterAggregateStandardInformation</i> is specified for an operating system prior to Windows Vista, <b>FilterFindFirst</b> returns this HRESULT value.
       

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NO_MORE_ITEMS)</b></dt>
</dl>
</td>
<td width="60%">
A filter driver was not found in the global list of registered filters.

</td>
</tr>
</table>

## -remarks

The <b>FilterFindFirst</b> function opens a search handle and returns information about the first filter driver that is found in the global list of registered filters. After the search handle has been established, call the <a href="/windows/desktop/api/fltuser/nf-fltuser-filterfindnext">FilterFindNext</a> function to search for other filters in the global list. When the search handle is no longer required, close it by calling <a href="/windows/desktop/api/fltuser/nf-fltuser-filterfindclose">FilterFindClose</a>. 

Starting with Microsoft Windows Server 2003 with SP1 and Windows XP with Service Pack 1 (SP1) with filter manager rollup, <b>FilterFindFirst</b> and <a href="/windows/desktop/api/fltuser/nf-fltuser-filterfindnext">FilterFindNext</a> can provide legacy filter driver information and minifilter driver instance information. On earlier versions of Windows, <b>FilterFindFirst</b> and <b>FilterFindNext</b> can only provide information about minifilters (see the description for the <i>dwInformationClass</i> parameter above).

<b>FilterFindFirst</b> and <a href="/windows/desktop/api/fltuser/nf-fltuser-filterfindnext">FilterFindNext</a> return information about filter drivers in order of decreasing distance from the base file system. Information about the filter farthest from the base file system is returned first.  Information about the second-farthest filter is returned second.  Information about the filter closest to the base file system is returned last.

If the input <i>dwBufferSize</i> is too small, <i>lpFilterFind</i> receives INVALID_HANDLE_VALUE, and <i>lpBytesReturned</i> receives the number of bytes required to store the requested information.

## -see-also

<a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_filter_aggregate_basic_information">FILTER_AGGREGATE_BASIC_INFORMATION</a>



<a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_filter_aggregate_standard_information">FILTER_AGGREGATE_STANDARD_INFORMATION</a>



<a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_filter_full_information">FILTER_FULL_INFORMATION</a>



<a href="/windows/desktop/api/fltuser/nf-fltuser-filterfindclose">FilterFindClose</a>



<a href="/windows/desktop/api/fltuser/nf-fltuser-filterfindnext">FilterFindNext</a>