---
UID: NF:mfidl.IMFVideoSampleAllocator.SetDirectXManager
title: IMFVideoSampleAllocator::SetDirectXManager (mfidl.h)
description: Specifies the Direct3D device manager for the video media sink to use.
helpviewer_keywords: ["IMFVideoSampleAllocator interface [Media Foundation]","SetDirectXManager method","IMFVideoSampleAllocator.SetDirectXManager","IMFVideoSampleAllocator::SetDirectXManager","SetDirectXManager","SetDirectXManager method [Media Foundation]","SetDirectXManager method [Media Foundation]","IMFVideoSampleAllocator interface","bad810c9-f5b1-42dc-9c7a-3306f3de2846","mf.imfvideosampleallocator_setdirectxmanager","mfidl/IMFVideoSampleAllocator::SetDirectXManager"]
old-location: mf\imfvideosampleallocator_setdirectxmanager.htm
tech.root: mf
ms.assetid: bad810c9-f5b1-42dc-9c7a-3306f3de2846
ms.date: 12/05/2018
ms.keywords: IMFVideoSampleAllocator interface [Media Foundation],SetDirectXManager method, IMFVideoSampleAllocator.SetDirectXManager, IMFVideoSampleAllocator::SetDirectXManager, SetDirectXManager, SetDirectXManager method [Media Foundation], SetDirectXManager method [Media Foundation],IMFVideoSampleAllocator interface, bad810c9-f5b1-42dc-9c7a-3306f3de2846, mf.imfvideosampleallocator_setdirectxmanager, mfidl/IMFVideoSampleAllocator::SetDirectXManager
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFVideoSampleAllocator::SetDirectXManager
 - mfidl/IMFVideoSampleAllocator::SetDirectXManager
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFVideoSampleAllocator.SetDirectXManager
---

# IMFVideoSampleAllocator::SetDirectXManager


## -description

Specifies the Direct3D device manager for the video media sink to use.

## -parameters

### -param pManager [in]

Pointer to the <b>IUnknown</b> interface of the Direct3D device manager. The media sink queries this pointer for the <a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9">IDirect3DDeviceManager9</a> interface.

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
</table>

## -remarks

The media sink uses the Direct3D device manager to obtain a pointer to the Direct3D device, which it uses to allocate Direct3D surfaces. The device manager enables multiple objects in the pipeline (such as a video renderer and a video decoder) to share the same Direct3D device.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator">IMFVideoSampleAllocator</a>