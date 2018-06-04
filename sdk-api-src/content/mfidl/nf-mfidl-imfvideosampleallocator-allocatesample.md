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

# IMFVideoSampleAllocator::AllocateSample


## -description


Gets a video sample from the allocator.
        


## -parameters




### -param ppSample [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a> interface. The caller must release the interface.
          


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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

                The method succeeded.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The allocator was not initialized. Call <a href="https://msdn.microsoft.com/b1e4557e-990c-4239-b9ec-5c7c46072e54">IMFVideoSampleAllocator::InitializeSampleAllocator</a> or <a href="https://msdn.microsoft.com/0AE0826D-058C-4A2F-94F2-A761CA885E67">InitializeSampleAllocatorEx::InitializeSampleAllocatorEx</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SAMPLEALLOCATOR_EMPTY</b></dt>
</dl>
</td>
<td width="60%">

                No samples are available.
              

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/bef92133-ae6c-4013-9210-5e0f0be2002c">IMFVideoSampleAllocator</a>
 

 

