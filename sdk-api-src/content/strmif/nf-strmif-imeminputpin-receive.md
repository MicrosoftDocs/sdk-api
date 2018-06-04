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

# IMemInputPin::Receive


## -description



The <code>Receive</code> method receives the next media sample in the stream.




## -parameters




### -param pSample [in]

Pointer to the sample's <a href="https://msdn.microsoft.com/883e5e3b-db91-4806-96cc-c6f8cddfcca6">IMediaSample</a> interface.


## -returns



Returns an <b>HRESULT</b> value. Possible values include those shown in the following table.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The sample was rejected.

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
<dt><b>VFW_E_INVALIDMEDIATYPE</b></dt>
</dl>
</td>
<td width="60%">
Invalid media type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_RUNTIME_ERROR</b></dt>
</dl>
</td>
<td width="60%">
A run-time error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
The pin is stopped.

</td>
</tr>
</table>
 




## -remarks



This method is synchronous and possibly blocking. The pin does one of the following:

<ul>
<li>Rejects the sample.</li>
<li>Returns immediately and processes the sample in a worker thread.</li>
<li>Processes the sample before returning.</li>
</ul>
In the last case, the method might block indefinitely. If this might happen, the <a href="https://msdn.microsoft.com/cc047cad-e250-41f7-856d-26fc077f87a1">IMemInputPin::ReceiveCanBlock</a> method returns S_OK.

If the pin uses a worker thread to process the sample, it holds a reference count on the sample. In any case, the output pin cannot directly re-use this sample. It must call the <a href="https://msdn.microsoft.com/a5d015c8-ef15-4bac-906f-5d064fbff11f">IMemAllocator::GetBuffer</a> method to obtain a new sample.

If this method returns S_FALSE or an error code, the upstream filter should stop sending samples until the graph stops or completes a flush operation. Typical reasons for an S_FALSE return value include:

<ul>
<li>The downstream pin is flushing; that is, it received a <b>BeginFlush</b> call and has not yet received an <b>EndFlush</b> call.</li>
<li>The downstream filter detected the end of the stream. (See <a href="https://msdn.microsoft.com/cf2b13bc-5b54-4ac7-8a33-7434126fdf31">End-of-Stream Notifications</a>.)</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/a4407c6f-6bb5-4274-920b-8bf7d76268bc">IMemInputPin Interface</a>
 

 

