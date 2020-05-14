---
UID: NF:strmif.IEnumRegFilters.Next
title: IEnumRegFilters::Next (strmif.h)
description: Note  The IEnumRegFilters interface is deprecated. Fills the array with descriptions of the next set of filters (specified by the cFilters parameter) that meet the requirements specified upon creation of the enumerator.helpviewer_keywords: ["IEnumRegFilters interface [DirectShow]","Next method","IEnumRegFilters.Next","IEnumRegFilters::Next","IEnumRegFiltersNext","Next","Next method [DirectShow]","Next method [DirectShow]","IEnumRegFilters interface","dshow.ienumregfilters_next","strmif/IEnumRegFilters::Next"]
old-location: dshow\ienumregfilters_next.htm
tech.root: DirectShow
ms.assetid: ec255b9b-33cf-42a3-9f02-f1f34eee2da1
ms.date: 12/05/2018
ms.keywords: IEnumRegFilters interface [DirectShow],Next method, IEnumRegFilters.Next, IEnumRegFilters::Next, IEnumRegFiltersNext, Next, Next method [DirectShow], Next method [DirectShow],IEnumRegFilters interface, dshow.ienumregfilters_next, strmif/IEnumRegFilters::Next
f1_keywords:
- strmif/IEnumRegFilters.Next
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmif.h
api_name:
- IEnumRegFilters.Next
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumRegFilters::Next


## -description



<div class="alert"><b>Note</b>  The <b>IEnumRegFilters</b> interface is deprecated.</div>
<div> </div>
Fills the array with descriptions of the next set of filters (specified by the <i>cFilters</i> parameter) that meet the requirements specified upon creation of the enumerator.




## -parameters




### -param cFilters [in]

Number of filters.


### -param apRegFilter [out]

Address of a pointer to an array of <b>REGFILTER</b> pointers.


### -param pcFetched [out]

Pointer to the actual number of filters passed.


## -returns



Returns one of the following <b>HRESULT</b> values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Fewer filters were retrieved than requested.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_ENUM_OUT_OF_SYNC</b></dt>
</dl>
</td>
<td width="60%">
The enumerator has become invalid. For more information, see Remarks.

</td>
</tr>
</table>
 




## -remarks



The calling application must use the Microsoft Win32 <b>CoTaskMemFree</b> function to free each <b>REGFILTER</b> pointer returned in the array. Do not free the <b>Name</b> member of the <b>REGFILTER</b> structure separately, because <code>IEnumRegFilters::Next</code> allocates memory for this string as part of the <b>REGFILTER</b> structure.

If the number of registered filters changes, the state of the enumerator will no longer be consistent with the state of the registry. As a result, this method will return VFW_E_ENUM_OUT_OF_SYNC. You should discard any data obtained from previous calls to the enumerator, because it might be invalid, and update the enumerator by calling the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ienumregfilters-reset">Reset</a> method. You can then call the <code>Next</code> method safely.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ienumregfilters">IEnumRegFilters Interface</a>
 

 

