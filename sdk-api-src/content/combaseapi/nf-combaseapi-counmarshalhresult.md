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

# CoUnmarshalHresult function


## -description


Unmarshals an <b>HRESULT</b> type from the specified stream.


## -parameters




### -param pstm [in]

A pointer to the stream from which the <b>HRESULT</b> is to be unmarshaled.


### -param phresult [out]

A pointer to the unmarshaled <b>HRESULT</b>.


## -returns



This function can return the standard return values E_OUTOFMEMORY and E_UNEXPECTED, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The <b>HRESULT</b> was unmarshaled successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_INVALIDPOINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pStm</i> is an invalid pointer.


</td>
</tr>
</table>
 




## -remarks



You do not explicitly call this function unless you are performing custom marshaling (that is, writing your own implementation of <a href="https://msdn.microsoft.com/e6f08949-f27d-4aba-adff-eaf9c356a928">IMarshal</a>), and your implementation needs to unmarshal an <b>HRESULT</b>.

You must use <b>CoUnmarshalHresult</b> to unmarshal <b>HRESULT</b> values previously marshaled by a call to the <a href="https://msdn.microsoft.com/37aaf404-49ca-4881-a369-44c5288abf1d">CoMarshalHresult</a> function.

This function performs the following tasks:

<ol>
<li>
 an <b>HRESULT</b> from a stream.

</li>
<li>Returns the <b>HRESULT</b>.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/37aaf404-49ca-4881-a369-44c5288abf1d">CoMarshalHresult</a>



<a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>
 

 

