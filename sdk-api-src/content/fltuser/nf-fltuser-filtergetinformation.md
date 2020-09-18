---
UID: NF:fltuser.FilterGetInformation
title: FilterGetInformation function (fltuser.h)
description: The FilterGetInformation function returns various kinds of information about a minifilter.
helpviewer_keywords: ["FilterGetInformation","FilterGetInformation function [Installable File System Drivers]","FltWin32ApiRef_244d89a8-3a31-44bd-bc08-b3ea8bb4dbba.xml","fltuser/FilterGetInformation","ifsk.filtergetinformation"]
old-location: ifsk\filtergetinformation.htm
tech.root: ifsk
ms.assetid: d5124ac2-dd1e-46b2-b25c-e965768eaf9e
ms.date: 12/05/2018
ms.keywords: FilterGetInformation, FilterGetInformation function [Installable File System Drivers], FltWin32ApiRef_244d89a8-3a31-44bd-bc08-b3ea8bb4dbba.xml, fltuser/FilterGetInformation, ifsk.filtergetinformation
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
 - FilterGetInformation
 - fltuser/FilterGetInformation
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
 - FilterGetInformation
---

# FilterGetInformation function


## -description

The <b>FilterGetInformation</b> function returns various kinds of information about a minifilter.

## -parameters

### -param hFilter [in]

Handle returned by a previous call to the <a href="/windows/desktop/api/fltuser/nf-fltuser-filtercreate">FilterCreate</a> function.

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
Return a <a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_filter_full_information">FILTER_FULL_INFORMATION</a> structure for the minifilter. 

</td>
</tr>
<tr>
<td>
<b>FilterAggregateBasicInformation</b>

</td>
<td>
Return a <a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_filter_aggregate_basic_information">FILTER_AGGREGATE_BASIC_INFORMATION</a> structure for the minifilter. This <i>dwInformationClass</i> value is available starting with Microsoft Windows Server 2003 with SP1 and Microsoft Windows XP with SP2 with filter manager rollup.  For more information about the filter manager rollup package for Windows XP with SP2, see article 914882, " <a href="https://support.microsoft.com/?kbid&amp;ID=914882">The filter manager rollup package for Windows XP SP2</a>," in the Microsoft Knowledge Base. 

</td>
</tr>
<tr>
<td>
<b>FilterAggregateStandardInformation</b>

</td>
<td>
Return a <a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_filter_aggregate_standard_information">FILTER_AGGREGATE_STANDARD_INFORMATION</a> structure for each minifilter. The LegacyFilter portion of the structure is not utilized.  This <i>dwInformationClass</i> value is available starting with Windows Vista.

</td>
</tr>
</table>

### -param lpBuffer [out]

Pointer to a caller-allocated buffer that receives the requested information. The type of the information returned in the buffer is defined by the <i>dwInformationClass</i> parameter.

### -param dwBufferSize [in]

Size, in bytes, of the buffer that the <i>lpBuffer</i> parameter points to. The caller should set this parameter according to the given <i>dwInformationClass</i>.

### -param lpBytesReturned [out]

Pointer to a caller-allocated variable that receives the number of bytes returned in the buffer that <i>lpBuffer</i> points to if the call to <b>FilterGetInformation</b> succeeds. This parameter is required and cannot be <b>NULL</b>.

## -returns

<b>FilterGetInformation</b> returns S_OK if successful. Otherwise, it returns an HRESULT error value, such as one of the following:

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
An invalid value was specified for the <i>dwInformationClass</i> parameter.  For example, if <b>FilterAggregateStandardInformation</b> is specified for an operating system prior to Windows Vista, <b>FilterGetInformation</b> returns this HRESULT value.
       

</td>
</tr>
</table>

## -remarks

<b>FilterGetInformation</b> is the Win32 equivalent of <a href="/windows-hardware/drivers/ddi/content/fltkernel/nf-fltkernel-fltgetfilterinformation">FltGetFilterInformation</a>.

## -see-also

<a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_filter_aggregate_basic_information">FILTER_AGGREGATE_BASIC_INFORMATION</a>



<a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_filter_aggregate_standard_information">FILTER_AGGREGATE_STANDARD_INFORMATION</a>



<a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_filter_full_information">FILTER_FULL_INFORMATION</a>



<a href="/windows/desktop/api/fltuser/nf-fltuser-filtercreate">FilterCreate</a>



<a href="/windows-hardware/drivers/ddi/content/fltkernel/nf-fltkernel-fltgetfilterinformation">FltGetFilterInformation</a>