---
UID: NF:mfapi.MFCreateVideoSampleAllocatorEx
title: MFCreateVideoSampleAllocatorEx function (mfapi.h)
description: Creates an object that allocates video samples that are compatible with Microsoft DirectX Graphics Infrastructure (DXGI).
helpviewer_keywords: ["IID_IMFVideoSampleAllocator","IID_IMFVideoSampleAllocatorCallback","IID_IMFVideoSampleAllocatorEx","IID_IUnknown","MFCreateVideoSampleAllocatorEx","MFCreateVideoSampleAllocatorEx function [Media Foundation]","mf.mfcreatevideosampleallocatorex","mfapi/MFCreateVideoSampleAllocatorEx"]
old-location: mf\mfcreatevideosampleallocatorex.htm
tech.root: mf
ms.assetid: AB2A4D0B-CDE0-462C-BF52-3F78D0093526
ms.date: 12/05/2018
ms.keywords: IID_IMFVideoSampleAllocator, IID_IMFVideoSampleAllocatorCallback, IID_IMFVideoSampleAllocatorEx, IID_IUnknown, MFCreateVideoSampleAllocatorEx, MFCreateVideoSampleAllocatorEx function [Media Foundation], mf.mfcreatevideosampleallocatorex, mfapi/MFCreateVideoSampleAllocatorEx
req.header: mfapi.h
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
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateVideoSampleAllocatorEx
 - mfapi/MFCreateVideoSampleAllocatorEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCreateVideoSampleAllocatorEx
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
<dt><b>IID_IUnknown</b></dt>
</dl>
</td>
<td width="60%">
Retrieve an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer.

</td>
</tr>
<tr>
<td width="40%"><a id="IID_IMFVideoSampleAllocator"></a><a id="iid_imfvideosampleallocator"></a><a id="IID_IMFVIDEOSAMPLEALLOCATOR"></a><dl>
<dt><b>IID_IMFVideoSampleAllocator</b></dt>
</dl>
</td>
<td width="60%">
Retrieve an <a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator">IMFVideoSampleAllocator</a> pointer.

</td>
</tr>
<tr>
<td width="40%"><a id="IID_IMFVideoSampleAllocatorEx"></a><a id="iid_imfvideosampleallocatorex"></a><a id="IID_IMFVIDEOSAMPLEALLOCATOREX"></a><dl>
<dt><b>IID_IMFVideoSampleAllocatorEx</b></dt>
</dl>
</td>
<td width="60%">
Retrieve an <a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex">IMFVideoSampleAllocatorEx</a> pointer.

</td>
</tr>
<tr>
<td width="40%"><a id="IID_IMFVideoSampleAllocatorCallback"></a><a id="iid_imfvideosampleallocatorcallback"></a><a id="IID_IMFVIDEOSAMPLEALLOCATORCALLBACK"></a><dl>
<dt><b>IID_IMFVideoSampleAllocatorCallback</b></dt>
</dl>
</td>
<td width="60%">
Retrieve an <a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorcallback">IMFVideoSampleAllocatorCallback</a> pointer.

</td>
</tr>
</table>

### -param ppSampleAllocator [out]

Receives a pointer to the requested interface. The caller must release the interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function creates an allocator for DXGI video surfaces. The buffers created by this allocator expose the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgibuffer">IMFDXGIBuffer</a> interface. To create an allocator for Microsoft Direct3D 9 video surfaces, call <a href="/windows/desktop/api/evr/nc-evr-mfcreatevideosampleallocator">MFCreateVideoSampleAllocator</a>.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>