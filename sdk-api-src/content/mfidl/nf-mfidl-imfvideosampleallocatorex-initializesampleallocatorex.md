---
UID: NF:mfidl.IMFVideoSampleAllocatorEx.InitializeSampleAllocatorEx
title: IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx
author: windows-sdk-content
description: Initializes the video sample allocator object.
old-location: mf\imfvideosampleallocatorex_initializesampleallocatorex.htm
old-project: medfound
ms.assetid: 0AE0826D-058C-4A2F-94F2-A761CA885E67
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IMFVideoSampleAllocatorEx interface [Media Foundation],InitializeSampleAllocatorEx method, IMFVideoSampleAllocatorEx.InitializeSampleAllocatorEx, IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx, InitializeSampleAllocatorEx, InitializeSampleAllocatorEx method [Media Foundation], InitializeSampleAllocatorEx method [Media Foundation],IMFVideoSampleAllocatorEx interface, mf.imfvideosampleallocatorex_initializesampleallocatorex, mfidl/IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: MFSensorDeviceMode
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
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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

A pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface. You can use this interface to configure the allocator. Currently, the following configuration attributes are defined:

<ul>
<li>
<a href="https://msdn.microsoft.com/A782BF8A-822A-407D-A30A-F2045BBB0BC0">MF_SA_BUFFERS_PER_SAMPLE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/C3B475B1-9A44-47EA-BCE7-D3D0FB56DDAC">MF_SA_D3D11_BINDFLAGS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/E9A415FA-74BF-4822-BB0E-D8AAA7D73664">MF_SA_D3D11_USAGE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/798CA474-3B1A-4795-81B7-563749197104">MF_SA_D3D11_SHARED</a>
</li>
<li>
<a href="https://msdn.microsoft.com/A9F4D4AF-BB47-48E2-B40A-D0245FD61FAF">MF_SA_D3D11_SHARED_WITHOUT_MUTEX</a>
</li>
</ul>

### -param pMediaType [in]

A pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface of a media type that describes the video format. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/B621F413-001B-4419-8FA7-439C45F97243">IMFVideoSampleAllocatorEx</a>
 

 

