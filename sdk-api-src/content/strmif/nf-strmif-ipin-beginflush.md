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

# IPin::BeginFlush


## -description



The <code>BeginFlush</code> method begins a flush operation.



Applications should not call this method. This method is called by other filters, to flush data from the graph.


## -parameters






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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The pin is an output pin.

</td>
</tr>
</table>
 




## -remarks



Call this method only on input pins. Output pins return E_UNEXPECTED.

In a flush operation, a filter discards whatever data it was processing. It rejects new data until the flush is completed. The flush is completed when the upstream pin calls the <a href="https://msdn.microsoft.com/42b201b6-1fbf-4a01-aed7-23a9e66c11ea">IPin::EndFlush</a> method. Flushing enables the filter graph to be more responsive when events alter the normal data flow. For example, flushing occurs during a seek.

When <code>BeginFlush</code> is called, the filter performs the following steps:

<ol>
<li>Passes the <code>IPin::BeginFlush</code> call downstream.</li>
<li>Sets an internal flag that causes all data-streaming methods to fail, such as <a href="https://msdn.microsoft.com/7cc1e57a-a18a-4ea4-9669-0be3fb140d40">IMemInputPin::Receive</a>.</li>
<li>Returns from any blocked calls to the <a href="https://msdn.microsoft.com/7cc1e57a-a18a-4ea4-9669-0be3fb140d40">Receive</a> method.</li>
</ol>
When the <code>BeginFlush</code> notification reaches a renderer filter, the renderer frees any samples that it holds.

After <code>BeginFlush</code> is called, the pin rejects all samples from upstream, with a return value of S_FALSE, until the <a href="https://msdn.microsoft.com/42b201b6-1fbf-4a01-aed7-23a9e66c11ea">IPin::EndFlush</a> method is called.




## -see-also




<a href="https://msdn.microsoft.com/3fcfd874-39bc-42d2-9fc9-2d8945ffa8e3">Data Flow in the Filter Graph</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/ad0ead4e-9f8e-4935-b220-306d665e50f4">IPin Interface</a>
 

 

