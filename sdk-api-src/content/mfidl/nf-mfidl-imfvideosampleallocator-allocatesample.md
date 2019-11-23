---
UID: NF:mfidl.IMFVideoSampleAllocator.AllocateSample
title: IMFVideoSampleAllocator::AllocateSample (mfidl.h)

description: Gets a video sample from the allocator.
old-location: mf\imfvideosampleallocator_allocatesample.htm
tech.root: medfound
ms.assetid: e5347cef-edbd-4f6a-88c9-042e53515a32

ms.date: 12/05/2018
ms.keywords: AllocateSample, AllocateSample method [Media Foundation], AllocateSample method [Media Foundation],IMFVideoSampleAllocator interface, IMFVideoSampleAllocator interface [Media Foundation],AllocateSample method, IMFVideoSampleAllocator.AllocateSample, IMFVideoSampleAllocator::AllocateSample, e5347cef-edbd-4f6a-88c9-042e53515a32, mf.imfvideosampleallocator_allocatesample, mfidl/IMFVideoSampleAllocator::AllocateSample
ms.topic: method
f1_keywords: 
 - "mfidl/IMFVideoSampleAllocator.AllocateSample"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFVideoSampleAllocator::AllocateSample


## -description


Gets a video sample from the allocator.
        


## -parameters




### -param ppSample [out]

Receives a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a> interface. The caller must release the interface.
          


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
The allocator was not initialized. Call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocator-initializesampleallocator">IMFVideoSampleAllocator::InitializeSampleAllocator</a> or <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex">InitializeSampleAllocatorEx::InitializeSampleAllocatorEx</a>.

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




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator">IMFVideoSampleAllocator</a>
 

 

