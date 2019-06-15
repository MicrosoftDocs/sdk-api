---
UID: NF:mfidl.IMFVideoSampleAllocatorEx.InitializeSampleAllocatorEx
title: IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx (mfidl.h)
author: windows-sdk-content
description: Initializes the video sample allocator object.
old-location: mf\imfvideosampleallocatorex_initializesampleallocatorex.htm
tech.root: medfound
ms.assetid: 0AE0826D-058C-4A2F-94F2-A761CA885E67
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFVideoSampleAllocatorEx interface [Media Foundation],InitializeSampleAllocatorEx method, IMFVideoSampleAllocatorEx.InitializeSampleAllocatorEx, IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx, InitializeSampleAllocatorEx, InitializeSampleAllocatorEx method [Media Foundation], InitializeSampleAllocatorEx method [Media Foundation],IMFVideoSampleAllocatorEx interface, mf.imfvideosampleallocatorex_initializesampleallocatorex, mfidl/IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx
ms.topic: method
f1_keywords: ["mfidl/IMFVideoSampleAllocatorEx.InitializeSampleAllocatorEx"]
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - mfidl.h
api_name:
 - IMFVideoSampleAllocatorEx.InitializeSampleAllocatorEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx


## -description


Initializes the video sample allocator object.


## -parameters




### -param cInitialSamples [in]

The initial number of samples to allocate. 


### -param cMaximumSamples [in]

The maximum number of samples to allocate.


### -param pAttributes [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface. You can use this interface to configure the allocator. Currently, the following configuration attributes are defined:

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/medfound/mf-sa-buffers-per-sample">MF_SA_BUFFERS_PER_SAMPLE</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/medfound/mf-sa-d3d11-bindflags">MF_SA_D3D11_BINDFLAGS</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/medfound/mf-sa-d3d11-usage">MF_SA_D3D11_USAGE</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/medfound/mf-sa-d3d11-shared">MF_SA_D3D11_SHARED</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/medfound/mf-sa-d3d11-shared-without-mutex">MF_SA_D3D11_SHARED_WITHOUT_MUTEX</a>
</li>
</ul>

### -param pMediaType [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface of a media type that describes the video format. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex">IMFVideoSampleAllocatorEx</a>
 

 

