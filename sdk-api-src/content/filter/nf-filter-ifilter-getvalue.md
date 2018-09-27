---
UID: NF:filter.IFilter.GetValue
title: IFilter::GetValue
author: windows-sdk-content
description: Retrieves a value (internal value-type property) from a chunk, which must have a CHUNKSTATE enumeration value of CHUNK_VALUE.
old-location: indexsrv\ifilter_getvalue.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_1cpx.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetValue, GetValue method [Indexing Service], GetValue method [Indexing Service],IFilter interface, IFilter interface [Indexing Service],GetValue method, IFilter.GetValue, IFilter::GetValue, _idxs_IFilter_GetValue, filter/IFilter::GetValue, indexsrv.ifilter_getvalue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: filter.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Filter.h
api_name:
 - IFilter.GetValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFilter::GetValue


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/en-us/library/Aa965362(v=VS.85).aspx">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Retrieves a value (internal value-type property) from a chunk, which must have a <a href="https://msdn.microsoft.com/en-us/library/ms691020(v=VS.85).aspx">CHUNKSTATE</a> enumeration value of CHUNK_VALUE.



## -parameters




### -param ppPropValue [out]

A pointer to an output variable that receives a pointer to the <a href="https://msdn.microsoft.com/en-us/library/Aa380072(v=VS.85).aspx">PROPVARIANT</a> structure that contains the value-type property. 


## -returns



This method can return one of these values.

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
The operation was completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FILTER_E_NO_MORE_VALUES </b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/en-us/library/ms690927(v=VS.85).aspx">GetValue</a> method has already been called on this chunk; this value should be returned until the <a href="https://msdn.microsoft.com/en-us/library/ms691080(v=VS.85).aspx">IFilter::GetChunk</a> method has been called successfully and has advanced to the next chunk.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FILTER_E_NO_VALUES</b></dt>
</dl>
</td>
<td width="60%">
The current chunk does not have a <a href="https://msdn.microsoft.com/en-us/library/ms691020(v=VS.85).aspx">CHUNKSTATE</a> enumeration value of CHUNK_VALUE. 

</td>
</tr>
</table>
 




## -remarks



Call the <b>GetValue</b> method only once per chunk. 



Note that the effect of producing the same value from more than one chunk is undefined. Only the last setting of the value is valid.



<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Allocate the <a href="https://msdn.microsoft.com/en-us/library/Aa380072(v=VS.85).aspx">PROPVARIANT</a> structure with <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a>. Some <b>PROPVARIANT</b> structures contain pointers, which can be freed by calling the <a href="https://msdn.microsoft.com/en-us/library/Aa380073(v=VS.85).aspx">PropVariantClear</a> function. It is up to the caller of the <b>GetValue</b> method to call <b>PropVariantClear</b>.






## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691105(v=VS.85).aspx">IFilter</a>
 

 

