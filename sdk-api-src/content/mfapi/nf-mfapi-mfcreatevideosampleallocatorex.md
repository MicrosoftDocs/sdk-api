---
UID: NF:mfapi.MFCreateVideoSampleAllocatorEx
title: MFCreateVideoSampleAllocatorEx function
author: windows-driver-content
description: Creates an object that allocates video samples that are compatible with Microsoft DirectX Graphics Infrastructure (DXGI).
old-location: mf\mfcreatevideosampleallocatorex.htm
old-project: medfound
ms.assetid: AB2A4D0B-CDE0-462C-BF52-3F78D0093526
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: IID_IMFVideoSampleAllocator, IID_IMFVideoSampleAllocatorCallback, IID_IMFVideoSampleAllocatorEx, IID_IUnknown, MFCreateVideoSampleAllocatorEx, MFCreateVideoSampleAllocatorEx function [Media Foundation], mf.mfcreatevideosampleallocatorex, mfapi/MFCreateVideoSampleAllocatorEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfapi.h
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
req.typenames: MF_CUSTOM_DECODE_UNIT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mfplat.dll
api_name:
-	MFCreateVideoSampleAllocatorEx
product: Windows
targetos: Windows
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFCreateVideoSampleAllocatorEx function


## -description


Creates an object that allocates video samples that are compatible with Microsoft DirectX Graphics Infrastructure (DXGI).


## -parameters




### -param riid [in]

The identifier of the interface to retrieve. Specify one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IID_IUnknown"></a><a id="iid_iunknown"></a><a id="IID_IUNKNOWN"></a><dl>
<dt><b><b>IID_IUnknown</b></b></dt>
</dl>
</td>
<td width="60%">
Retrieve an <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> pointer.

</td>
</tr>
<tr>
<td width="40%"><a id="IID_IMFVideoSampleAllocator"></a><a id="iid_imfvideosampleallocator"></a><a id="IID_IMFVIDEOSAMPLEALLOCATOR"></a><dl>
<dt><b><b>IID_IMFVideoSampleAllocator</b></b></dt>
</dl>
</td>
<td width="60%">
Retrieve an <a href="https://msdn.microsoft.com/bef92133-ae6c-4013-9210-5e0f0be2002c">IMFVideoSampleAllocator</a> pointer.

</td>
</tr>
<tr>
<td width="40%"><a id="IID_IMFVideoSampleAllocatorEx"></a><a id="iid_imfvideosampleallocatorex"></a><a id="IID_IMFVIDEOSAMPLEALLOCATOREX"></a><dl>
<dt><b><b>IID_IMFVideoSampleAllocatorEx</b></b></dt>
</dl>
</td>
<td width="60%">
Retrieve an <a href="https://msdn.microsoft.com/B621F413-001B-4419-8FA7-439C45F97243">IMFVideoSampleAllocatorEx</a> pointer.

</td>
</tr>
<tr>
<td width="40%"><a id="IID_IMFVideoSampleAllocatorCallback"></a><a id="iid_imfvideosampleallocatorcallback"></a><a id="IID_IMFVIDEOSAMPLEALLOCATORCALLBACK"></a><dl>
<dt><b><b>IID_IMFVideoSampleAllocatorCallback</b></b></dt>
</dl>
</td>
<td width="60%">
Retrieve an <a href="https://msdn.microsoft.com/7dbf8b3a-24b3-41d9-bb1e-9c57b88a77ac">IMFVideoSampleAllocatorCallback</a> pointer.

</td>
</tr>
</table>
 


### -param ppSampleAllocator [out]

Receives a pointer to the requested interface. The caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function creates an allocator for DXGI video surfaces. The buffers created by this allocator expose the <a href="https://msdn.microsoft.com/796D7755-275D-4A0B-A34F-5D34DCEC8AC7">IMFDXGIBuffer</a> interface. To create an allocator for Microsoft Direct3D 9 video surfaces, call <a href="https://msdn.microsoft.com/2d40a335-9948-40d9-b93f-18a6decf96c8">MFCreateVideoSampleAllocator</a>.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

