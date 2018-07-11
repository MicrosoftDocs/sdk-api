---
UID: NN:mfidl.IMFVideoSampleAllocatorEx
title: IMFVideoSampleAllocatorEx
author: windows-sdk-content
description: Allocates video samples that contain Microsoft Direct3D 11 texture surfaces.
old-location: mf\imfvideosampleallocatorex.htm
old-project: medfound
ms.assetid: B621F413-001B-4419-8FA7-439C45F97243
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IMFVideoSampleAllocatorEx, IMFVideoSampleAllocatorEx interface [Media Foundation], IMFVideoSampleAllocatorEx interface [Media Foundation],described, mf.imfvideosampleallocatorex, mfidl/IMFVideoSampleAllocatorEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
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
 - IMFVideoSampleAllocatorEx
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: Mfsensorgroup.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFVideoSampleAllocatorEx interface


## -description


Allocates video samples that contain Microsoft Direct3D 11 texture surfaces.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFVideoSampleAllocatorEx</b> interface inherits from <a href="https://msdn.microsoft.com/bef92133-ae6c-4013-9210-5e0f0be2002c">IMFVideoSampleAllocator</a>. <b>IMFVideoSampleAllocatorEx</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/0AE0826D-058C-4A2F-94F2-A761CA885E67">InitializeSampleAllocatorEx</a>
</td>
<td align="left" width="63%">
Initializes the video sample allocator object.

</td>
</tr>
</table> 


## -remarks



You can use this interface to allocateDirect3D 11 video samples, rather than allocate the texture surfaces and media samples directly. To get a pointer to this interface, call the <a href="https://msdn.microsoft.com/AB2A4D0B-CDE0-462C-BF52-3F78D0093526">MFCreateVideoSampleAllocatorEx</a> function. 

To allocate video samples, perform the following steps:

<ol>
<li>Obtain a pointer to the <a href="https://msdn.microsoft.com/4A0DC266-FCF0-4ECD-AC78-CF429839486D">IMFDXGIDeviceManager</a> interface. For a Media Foundation transform (MFT), this step occurs during the <a href="https://msdn.microsoft.com/fd346d56-1f80-488a-94c8-4e4e36d72890">MFT_MESSAGE_SET_D3D_MANAGER</a> event.</li>
<li>Call <a href="https://msdn.microsoft.com/AB2A4D0B-CDE0-462C-BF52-3F78D0093526">MFCreateVideoSampleAllocatorEx</a> to create the allocator object and get a pointer to the <b>IMFVideoSampleAllocatorEx</b> interface.</li>
<li>Call <a href="https://msdn.microsoft.com/bad810c9-f5b1-42dc-9c7a-3306f3de2846">IMFVideoSampleAllocator::SetDirectXManager</a> on the allocator to set the <a href="https://msdn.microsoft.com/4A0DC266-FCF0-4ECD-AC78-CF429839486D">IMFDXGIDeviceManager</a> pointer on the allocator.</li>
<li>Call <a href="https://msdn.microsoft.com/a79b1edd-5ca1-4550-a6ce-58073155affd">MFCreateAttributes</a> to get a pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface.</li>
<li>Set the <a href="https://msdn.microsoft.com/E9A415FA-74BF-4822-BB0E-D8AAA7D73664">MF_SA_D3D11_USAGE</a> and <a href="https://msdn.microsoft.com/C3B475B1-9A44-47EA-BCE7-D3D0FB56DDAC">MF_SA_D3D11_BINDFLAGS</a> attributes.</li>
<li>Call <a href="https://msdn.microsoft.com/0AE0826D-058C-4A2F-94F2-A761CA885E67">IMFVideoSampleAllocator::InitializeSampleAllocatorEx</a>.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/bef92133-ae6c-4013-9210-5e0f0be2002c">IMFVideoSampleAllocator</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

