---
UID: NC:evr.MFCreateVideoSampleAllocator
title: MFCreateVideoSampleAllocator (evr.h)
description: Creates an object that allocates video samples.
helpviewer_keywords: ["IID_IMFVideoSampleAllocator","IID_IMFVideoSampleAllocatorCallback","IID_IUnknown","MFCreateVideoSampleAllocator","MFCreateVideoSampleAllocator callback","MFCreateVideoSampleAllocator callback function [Media Foundation]","evr/MFCreateVideoSampleAllocator","mf.mfcreatevideosampleallocator"]
old-location: mf\mfcreatevideosampleallocator.htm
tech.root: mf
ms.assetid: 2d40a335-9948-40d9-b93f-18a6decf96c8
ms.date: 12/05/2018
ms.keywords: IID_IMFVideoSampleAllocator, IID_IMFVideoSampleAllocatorCallback, IID_IUnknown, MFCreateVideoSampleAllocator, MFCreateVideoSampleAllocator callback, MFCreateVideoSampleAllocator callback function [Media Foundation], evr/MFCreateVideoSampleAllocator, mf.mfcreatevideosampleallocator
req.header: evr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateVideoSampleAllocator
 - evr/MFCreateVideoSampleAllocator
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - evr.h
api_name:
 - MFCreateVideoSampleAllocator
---

# MFCreateVideoSampleAllocator callback function


## -description

Creates an object that allocates video samples.

## -parameters

### -param riid [in]

The identifier of the interface to retrieve. Specify one of the following values:

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
Retrieve an <b>IUnknown</b> pointer.

</td>
</tr>
<tr>
<td width="40%"><a id="IID_IMFVideoSampleAllocator"></a><a id="iid_imfvideosampleallocator"></a><a id="IID_IMFVIDEOSAMPLEALLOCATOR"></a><dl>
<dt><b><b>IID_IMFVideoSampleAllocator</b></b></dt>
</dl>
</td>
<td width="60%">
Retrieve an <a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator">IMFVideoSampleAllocator</a> pointer.

</td>
</tr>
<tr>
<td width="40%"><a id="IID_IMFVideoSampleAllocatorCallback"></a><a id="iid_imfvideosampleallocatorcallback"></a><a id="IID_IMFVIDEOSAMPLEALLOCATORCALLBACK"></a><dl>
<dt><b><b>IID_IMFVideoSampleAllocatorCallback</b></b></dt>
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

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Functions</a>