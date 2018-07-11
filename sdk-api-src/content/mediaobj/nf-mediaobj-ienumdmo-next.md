---
UID: NF:mediaobj.IEnumDMO.Next
title: IEnumDMO::Next
author: windows-sdk-content
description: The Next method retrieves a specified number of items in the enumeration sequence.
old-location: dshow\ienumdmo_next.htm
old-project: DirectShow
ms.assetid: 5094f2d3-caa7-4085-aebe-306a7b05b591
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: IEnumDMO interface [DirectShow],Next method, IEnumDMO.Next, IEnumDMO::Next, IEnumDMONext, Next, Next method [DirectShow], Next method [DirectShow],IEnumDMO interface, dshow.ienumdmo_next, mediaobj/IEnumDMO::Next
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mediaobj.h
req.include-header: Dmo.h
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IEnumDMO.Next
product: Windows
targetos: Windows
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
 

 

