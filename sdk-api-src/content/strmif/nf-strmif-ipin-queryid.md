---
UID: NF:strmif.IPin.QueryId
title: IPin::QueryId
author: windows-sdk-content
description: The QueryId method retrieves an identifier for the pin.
old-location: dshow\ipin_queryid.htm
tech.root: DirectShow
ms.assetid: d4fb2713-549d-4c0d-9768-386bcffd696f
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IPin interface [DirectShow],QueryId method, IPin.QueryId, IPin::QueryId, IPinQueryId, QueryId, QueryId method [DirectShow], QueryId method [DirectShow],IPin interface, dshow.ipin_queryid, strmif/IPin::QueryId
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IPin.QueryId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPin::QueryId


## -description



The <code>QueryId</code> method retrieves an identifier for the pin.




## -parameters




### -param Id [out]

Receives a string containing the pin identifier.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

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
Success.

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
</table>
 




## -remarks



This method supports graph persistence. Use this method to save a pin's state, and the <a href="https://msdn.microsoft.com/0bdefaeb-f631-4b79-9965-c1c570e0ff80">IBaseFilter::FindPin</a> method to restore the state. The pin's identifier string is defined by the filter implementation. The identifier must be unique within the filter.

<div class="alert"><b>Note</b>  The <i>pin identifier</i> is not necessarily the same as the <i>pin name</i> that the <a href="https://msdn.microsoft.com/1a7c85ce-46f1-4928-9e2a-3a4bd96dc771">QueryPinInfo</a> method returns.</div>
<div> </div>
The filter allocates the returned string using the <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a> function. The caller must free it using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.




## -see-also




<a href="https://msdn.microsoft.com/3fcfd874-39bc-42d2-9fc9-2d8945ffa8e3">Data Flow in the Filter Graph</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/ad0ead4e-9f8e-4935-b220-306d665e50f4">IPin Interface</a>
 

 

