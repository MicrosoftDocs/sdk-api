---
UID: NF:mfidl.IMFVideoSampleAllocator.InitializeSampleAllocator
title: IMFVideoSampleAllocator::InitializeSampleAllocator (mfidl.h)
author: windows-sdk-content
description: Specifies the number of samples to allocate and the media type for the samples.
old-location: mf\imfvideosampleallocator_initializesampleallocator.htm
tech.root: medfound
ms.assetid: b1e4557e-990c-4239-b9ec-5c7c46072e54
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFVideoSampleAllocator interface [Media Foundation],InitializeSampleAllocator method, IMFVideoSampleAllocator.InitializeSampleAllocator, IMFVideoSampleAllocator::InitializeSampleAllocator, InitializeSampleAllocator, InitializeSampleAllocator method [Media Foundation], InitializeSampleAllocator method [Media Foundation],IMFVideoSampleAllocator interface, b1e4557e-990c-4239-b9ec-5c7c46072e54, mf.imfvideosampleallocator_initializesampleallocator, mfidl/IMFVideoSampleAllocator::InitializeSampleAllocator
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
 - IMFVideoSampleAllocator.InitializeSampleAllocator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFVideoSampleAllocator::InitializeSampleAllocator


## -description


Specifies the number of samples to allocate and the media type for the samples.
        


## -parameters




### -param cRequestedFrames [in]

Number of samples to allocate.		
          


### -param pMediaType [in]

Pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface of a media type that describes the video format.
          


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
<dt><b>MF_E_INVALIDMEDIATYPE</b></dt>
</dl>
</td>
<td width="60%">
Invalid media type.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/bef92133-ae6c-4013-9210-5e0f0be2002c">IMFVideoSampleAllocator</a>
 

 

