---
UID: NF:mfidl.IMFVideoSampleAllocator.AllocateSample
title: IMFVideoSampleAllocator::AllocateSample
author: windows-sdk-content
description: Gets a video sample from the allocator.
old-location: mf\imfvideosampleallocator_allocatesample.htm
tech.root: medfound
ms.assetid: e5347cef-edbd-4f6a-88c9-042e53515a32
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: AllocateSample, AllocateSample method [Media Foundation], AllocateSample method [Media Foundation],IMFVideoSampleAllocator interface, IMFVideoSampleAllocator interface [Media Foundation],AllocateSample method, IMFVideoSampleAllocator.AllocateSample, IMFVideoSampleAllocator::AllocateSample, e5347cef-edbd-4f6a-88c9-042e53515a32, mf.imfvideosampleallocator_allocatesample, mfidl/IMFVideoSampleAllocator::AllocateSample
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFVideoSampleAllocator.AllocateSample
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

