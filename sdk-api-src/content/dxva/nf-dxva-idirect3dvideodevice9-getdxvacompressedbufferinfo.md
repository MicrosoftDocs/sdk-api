---
UID: NF:dxva.IDirect3DVideoDevice9.GetDXVACompressedBufferInfo
title: IDirect3DVideoDevice9::GetDXVACompressedBufferInfo method
author: windows-driver-content
description: Gets information about the compressed buffers needed for hardware-accelerated decoding.
old-location: mf\idirect3dvideodevice9_getdxvacompressedbufferinfo.htm
old-project: medfound
ms.assetid: 5a9fb077-fd79-4faa-a0f8-b3ac987adf36
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: GetDXVACompressedBufferInfo method [Media Foundation], GetDXVACompressedBufferInfo method [Media Foundation], IDirect3DVideoDevice9 interface, GetDXVACompressedBufferInfo,IDirect3DVideoDevice9.GetDXVACompressedBufferInfo, IDirect3DVideoDevice9, IDirect3DVideoDevice9 interface [Media Foundation], GetDXVACompressedBufferInfo method, IDirect3DVideoDevice9::GetDXVACompressedBufferInfo, dxva/IDirect3DVideoDevice9::GetDXVACompressedBufferInfo, mf.idirect3dvideodevice9_getdxvacompressedbufferinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dxva.h
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
req.typenames: COPP_TVProtectionStandard
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dxva.h
api_name:
-	IDirect3DVideoDevice9.GetDXVACompressedBufferInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDirect3DVideoDevice9::GetDXVACompressedBufferInfo method


## -description


Gets information about the compressed buffers needed for hardware-accelerated decoding.


## -parameters




### -param pGuid

Pointer to a GUID that specifies the DXVA profile. To get a list of supported profiles, call <a href="https://msdn.microsoft.com/4adbbac2-a25d-4e17-b62e-a02a67dcdbed">IDirect3DVideoDevice9::GetDXVAGuids</a>.


### -param pUncompData

Pointer to a <a href="https://msdn.microsoft.com/bd19d9a8-7d69-4aea-9638-84c3f1a1e810">DXVAUncompDataInfo</a> structure that specifies the size and pixel format of the uncompressed data.


### -param pNumBuffers

On input, specifies the number of elements in the <i>pBufferInfo</i> array.
            If <i>pBufferInfo</i> is <b>NULL</b>, the value of <code>*pNumBuffers</code> must be zero.

On output, if <i>pBufferInfo</i> is <b>NULL</b>, <i>pNumBuffers</i> receives the size of array to allocate. Otherwise, <i>pNumBuffers</i> receives the actual number of elements that are copied to the <i>pBufferInfo</i> array.


### -param pBufferInfo


            Address of an array of <a href="https://msdn.microsoft.com/dabef388-d883-48a6-9abc-218dc163ef63">DXVACompBufferInfo</a> structures or <b>NULL</b>. If the value is non-<b>NULL</b>, the method copies a list of <b>DXVACompBufferInfo</b> structures to this array. Each structure corresponds to one type of compressed data buffer that is used by the video accelerator.

Set all of the array elements to zero before calling this method.


            Each array index corresponds to one of the DXVA surface types defined in dxva.h. The video accelerator returns a list of up to <b>DXVA_NUM_TYPES_COMP_BUFFERS</b>
          array entries. For details, refer to the <a href="http://go.microsoft.com/fwlink/p/?linkid=93647">DXVA 1.0 specification</a>, section 3.4, "Buffer Description List." If a particular buffer type is not used by the DXVA profile, the entry at that index contains zeros for all values.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/abe3beac-f3f8-413d-8b83-9da3340b19ac">IDirect3DVideoDevice9</a>
 

 

