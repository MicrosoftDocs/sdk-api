---
UID: NN:mfidl.IMFVideoSampleAllocatorEx
title: IMFVideoSampleAllocatorEx (mfidl.h)
description: Allocates video samples that contain Microsoft Direct3D 11 texture surfaces.helpviewer_keywords: ["IMFVideoSampleAllocatorEx","IMFVideoSampleAllocatorEx interface [Media Foundation]","IMFVideoSampleAllocatorEx interface [Media Foundation]","described","mf.imfvideosampleallocatorex","mfidl/IMFVideoSampleAllocatorEx"]
old-location: mf\imfvideosampleallocatorex.htm
tech.root: medfound
ms.assetid: B621F413-001B-4419-8FA7-439C45F97243
ms.date: 12/05/2018
ms.keywords: IMFVideoSampleAllocatorEx, IMFVideoSampleAllocatorEx interface [Media Foundation], IMFVideoSampleAllocatorEx interface [Media Foundation],described, mf.imfvideosampleallocatorex, mfidl/IMFVideoSampleAllocatorEx
f1_keywords:
- mfidl/IMFVideoSampleAllocatorEx
dev_langs:
- c++
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
- IMFVideoSampleAllocatorEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFVideoSampleAllocatorEx interface


## -description


Allocates video samples that contain Microsoft Direct3D 11 texture surfaces.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFVideoSampleAllocatorEx</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator">IMFVideoSampleAllocator</a>. <b>IMFVideoSampleAllocatorEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFVideoSampleAllocatorEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex">InitializeSampleAllocatorEx</a>
</td>
<td align="left" width="63%">
Initializes the video sample allocator object.

</td>
</tr>
</table> 


## -remarks



You can use this interface to allocateDirect3D 11 video samples, rather than allocate the texture surfaces and media samples directly. To get a pointer to this interface, call the <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfcreatevideosampleallocatorex">MFCreateVideoSampleAllocatorEx</a> function. 

To allocate video samples, perform the following steps:

<ol>
<li>Obtain a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager">IMFDXGIDeviceManager</a> interface. For a Media Foundation transform (MFT), this step occurs during the <a href="https://docs.microsoft.com/windows/desktop/medfound/mft-message-set-d3d-manager">MFT_MESSAGE_SET_D3D_MANAGER</a> event.</li>
<li>Call <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfcreatevideosampleallocatorex">MFCreateVideoSampleAllocatorEx</a> to create the allocator object and get a pointer to the <b>IMFVideoSampleAllocatorEx</b> interface.</li>
<li>Call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocator-setdirectxmanager">IMFVideoSampleAllocator::SetDirectXManager</a> on the allocator to set the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager">IMFDXGIDeviceManager</a> pointer on the allocator.</li>
<li>Call <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes">MFCreateAttributes</a> to get a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface.</li>
<li>Set the <a href="https://docs.microsoft.com/windows/desktop/medfound/mf-sa-d3d11-usage">MF_SA_D3D11_USAGE</a> and <a href="https://docs.microsoft.com/windows/desktop/medfound/mf-sa-d3d11-bindflags">MF_SA_D3D11_BINDFLAGS</a> attributes.</li>
<li>Call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex">IMFVideoSampleAllocator::InitializeSampleAllocatorEx</a>.</li>
</ol>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator">IMFVideoSampleAllocator</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

