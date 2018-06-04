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

# CoMarshalHresult function


## -description


Marshals an <b>HRESULT</b> to the specified stream, from which it can be unmarshaled using the <a href="https://msdn.microsoft.com/a45ef72c-d385-4012-9683-7d2cc6d68b6d">CoUnmarshalHresult</a> function.




## -parameters




### -param pstm [in]

A pointer to the marshaling stream. See <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>.


### -param hresult [in]

The <b>HRESULT</b> in the originating process.


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
The <b>HRESULT</b> was marshaled successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_INVALIDPOINTER</b></dt>
</dl>
</td>
<td width="60%">
A bad pointer was specified for <i>pstm</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_MEDIUMFULL</b></dt>
</dl>
</td>
<td width="60%">
The medium is full.

</td>
</tr>
</table>
 




## -remarks



An <b>HRESULT</b> is process-specific, so an <b>HRESULT</b> that is valid in one process might not be valid in another. If you are writing your own implementation of <a href="https://msdn.microsoft.com/e6f08949-f27d-4aba-adff-eaf9c356a928">IMarshal</a> and need to marshal an <b>HRESULT</b> from one process to another, either as a parameter or a return code, you must call this function. In other circumstances, you will have no need to call this function.

This function performs the following tasks:

<ol>
<li>Writes an <b>HRESULT</b> to a stream.</li>
<li>Returns an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> pointer to that stream.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/a45ef72c-d385-4012-9683-7d2cc6d68b6d">CoUnmarshalHresult</a>



<a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>
 

 

