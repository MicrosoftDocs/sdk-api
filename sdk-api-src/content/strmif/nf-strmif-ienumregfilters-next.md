---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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

If the number of registered filters changes, the state of the enumerator will no longer be consistent with the state of the registry. As a result, this method will return VFW_E_ENUM_OUT_OF_SYNC. You should discard any data obtained from previous calls to the enumerator, because it might be invalid, and update the enumerator by calling the <a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a> method. You can then call the <code>Next</code> method safely.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/59cb809d-84f5-42c4-a385-0f586af4d048">IEnumRegFilters Interface</a>
 

 

