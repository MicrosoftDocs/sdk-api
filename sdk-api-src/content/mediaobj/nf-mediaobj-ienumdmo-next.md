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

# IEnumDMO::Next


## -description



The <code>Next</code> method retrieves a specified number of items in the enumeration sequence.




## -parameters




### -param cItemsToFetch

Number of items to retrieve.


### -param pCLSID [out]

Array of size <i>cItemsToFetch</i> that is filled with the CLSIDs of the enumerated DMOs.


### -param Names [out]

Array of size <i>cItemsToFetch</i> that is filled with the friendly names of the enumerated DMOs.


### -param pcItemsFetched [out]

Pointer to a variable that receives the actual number of items retrieved. Can be <b>NULL</b> if <i>cItemsToFetch</i> equals 1.


## -returns



Returns an <b>HRESULT</b> value. Possible values include those in the following table.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Retrieved fewer items than requested.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Retrieved the requested number of items.

</td>
</tr>
</table>
 




## -remarks



If the method succeeds, the arrays given by the <i>pCLSID</i> and <i>Names</i> parameters are filled with CLSIDs and wide-character strings. The value of *<i>pcItemsFetched</i> specifies the number of items returned in these arrays.

The method returns S_OK if it retrieves the requested number of items (in other words, if *<i>pcItemsFetched</i> equals <i>cItemsToFetch</i>). Otherwise, it returns S_FALSE or an error code.

The caller must free the memory allocated for each string returned in the <i>Names</i> parameter, using the <b>CoTaskMemFree</b> function.




## -see-also




<a href="https://msdn.microsoft.com/221248f2-5c8f-442e-a6ad-e0372ddc1aae">IEnumDMO Interface</a>
 

 

