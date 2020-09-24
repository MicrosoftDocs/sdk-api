---
UID: NF:fltuser.FilterFindNext
title: FilterFindNext function (fltuser.h)
description: The FilterFindNext function continues a filter search started by a call to FilterFindFirst.
helpviewer_keywords: ["FilterFindNext","FilterFindNext function [Installable File System Drivers]","FltWin32ApiRef_8f2234d4-aef1-47d3-9b9f-a43fbb309bef.xml","fltuser/FilterFindNext","ifsk.filterfindnext"]
old-location: ifsk\filterfindnext.htm
tech.root: ifsk
ms.assetid: ce56037b-d303-4efa-956f-6bbe5127efb7
ms.date: 12/05/2018
ms.keywords: FilterFindNext, FilterFindNext function [Installable File System Drivers], FltWin32ApiRef_8f2234d4-aef1-47d3-9b9f-a43fbb309bef.xml, fltuser/FilterFindNext, ifsk.filterfindnext
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
 - FilterFindNext
 - fltuser/FilterFindNext
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
 - FilterFindNext
---

# FilterFindNext function


## -description

The <b>FilterFindNext</b> function continues a filter search started by a call to <a href="/windows/desktop/api/fltuser/nf-fltuser-filterfindfirst">FilterFindFirst</a>.

## -parameters

### -param hFilterFind [in]

Filter search handle returned by a previous call to <a href="/windows/desktop/api/fltuser/nf-fltuser-filterfindfirst">FilterFindFirst</a>.

### -param dwInformationClass [in]

Type of information requested. This parameter must be one of the following values.

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
The buffer pointed to by the <i>lpBuffer</i> parameter receives a <a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_filter_aggregate_basic_information">FILTER_AGGREGATE_BASIC_INFORMATION</a> structure for each minifilter instance or legacy filter. This <i>dwInformationClass</i> value is available starting with Microsoft Windows Server 2003 with SP1 and Windows XP with SP2 with filter manager rollup.  For more information about the filter manager rollup package for Windows XP with SP2, see article 914882, " <a href="https://support.microsoft.com/?kbid&amp;ID=914882">The filter manager rollup package for Windows XP SP2</a>," in the Microsoft Knowledge Base.

</td>
</tr>
<tr>
<td>
<b>FilterAggregateStandardInformation</b>

</td>
<td>
The buffer pointed to by the <i>lpBuffer</i> parameter receives a <a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_filter_aggregate_standard_information">FILTER_AGGREGATE_STANDARD_INFORMATION</a> structure for each minifilter instance or legacy filter. This <i>dwInformationClass</i> value is available starting with Windows Vista.

</td>
</tr>
</table>

### -param lpBuffer [out]

Pointer to a caller-allocated buffer that receives the requested information. The type of the information returned is defined by the <i>dwInformationClass</i> parameter.

### -param dwBufferSize [in]

Size, in bytes, of the buffer that the <i>lpBuffer</i> parameter points to. The caller should set this parameter according to the given <i>dwInformationClass</i>.

### -param lpBytesReturned [out]

Pointer to a caller-allocated variable that receives the number of bytes returned in the buffer that <i>lpBuffer</i> points to if the call to <b>FilterFindNext</b> succeeds. This parameter is required and cannot be <b>NULL</b>.

## -returns

<b>FilterFindNext</b> returns S_OK if successful. Otherwise, it returns an HRESULT error value, such as one of the following:

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
An invalid value was specified for the <i>dwInformationClass</i> parameter.  For example, if <b>FilterAggregateStandardInformation</b> is specified for an operating system prior to Windows Vista, <b>FilterFindNext</b> returns this HRESULT value.
       

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NO_MORE_ITEMS)</b></dt>
</dl>
</td>
<td width="60%">
No more filter drivers were found in the global list of registered filter drivers.

</td>
</tr>
</table>

## -remarks

After the filter search handle is established by calling <a href="/windows/desktop/api/fltuser/nf-fltuser-filterfindfirst">FilterFindFirst</a>, use the <b>FilterFindNext</b> function to search for additional filters in the global list of registered filters. 

<b>FilterFindNext</b> finds one filter driver (minifilter driver instance or legacy filter driver) per call.

Starting with Microsoft Windows Server 2003 with SP1 and Microsoft Windows XP with SP2 with filter manager rollup, <a href="/windows/desktop/api/fltuser/nf-fltuser-filterfindfirst">FilterFindFirst</a> and <b>FilterFindNext</b> can provide legacy filter driver information and minifilter driver instance information. On earlier versions of Windows, <b>FilterFindFirst</b> and <b>FilterFindNext</b> can only provide information about minifilters (see the description for the <i>dwInformationClass</i> parameter above).


<a href="/windows/desktop/api/fltuser/nf-fltuser-filterfindfirst">FilterFindFirst</a> and <b>FilterFindNext</b> return information about filter drivers in order of decreasing distance from the base file system. Information about the filter farthest from the base file system is returned first.  Information about the second-farthest filter is returned second.  Information about the filter closest to the base file system is returned last.

## -see-also

<a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_filter_aggregate_basic_information">FILTER_AGGREGATE_BASIC_INFORMATION</a>



<a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_filter_aggregate_standard_information">FILTER_AGGREGATE_STANDARD_INFORMATION</a>



<a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_filter_full_information">FILTER_FULL_INFORMATION</a>



<a href="/windows/desktop/api/fltuser/nf-fltuser-filterfindclose">FilterFindClose</a>



<a href="/windows/desktop/api/fltuser/nf-fltuser-filterfindfirst">FilterFindFirst</a>