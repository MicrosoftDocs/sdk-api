---
UID: NE:mfidl.MFTOPOLOGY_DXVA_MODE
title: MFTOPOLOGY_DXVA_MODE (mfidl.h)
description: Specifies whether the topology loader enables Microsoft DirectX Video Acceleration (DXVA) in the topology.
helpviewer_keywords: ["MFTOPOLOGY_DXVA_DEFAULT","MFTOPOLOGY_DXVA_FULL","MFTOPOLOGY_DXVA_MODE","MFTOPOLOGY_DXVA_MODE enumeration [Media Foundation]","MFTOPOLOGY_DXVA_NONE","mf.mftopology_dxva_mode","mfidl/MFTOPOLOGY_DXVA_DEFAULT","mfidl/MFTOPOLOGY_DXVA_FULL","mfidl/MFTOPOLOGY_DXVA_MODE","mfidl/MFTOPOLOGY_DXVA_NONE"]
old-location: mf\mftopology_dxva_mode.htm
tech.root: mf
ms.assetid: c47f505a-1b98-4309-b462-5b911e1f591f
ms.date: 12/05/2018
ms.keywords: MFTOPOLOGY_DXVA_DEFAULT, MFTOPOLOGY_DXVA_FULL, MFTOPOLOGY_DXVA_MODE, MFTOPOLOGY_DXVA_MODE enumeration [Media Foundation], MFTOPOLOGY_DXVA_NONE, mf.mftopology_dxva_mode, mfidl/MFTOPOLOGY_DXVA_DEFAULT, mfidl/MFTOPOLOGY_DXVA_FULL, mfidl/MFTOPOLOGY_DXVA_MODE, mfidl/MFTOPOLOGY_DXVA_NONE
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: MFTOPOLOGY_DXVA_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFTOPOLOGY_DXVA_MODE
 - mfidl/MFTOPOLOGY_DXVA_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MFTOPOLOGY_DXVA_MODE
---

# MFTOPOLOGY_DXVA_MODE enumeration


## -description

Specifies whether the topology loader enables Microsoft DirectX Video Acceleration (DXVA) in the topology.

## -enum-fields

### -field MFTOPOLOGY_DXVA_DEFAULT:0

The topology loader enables DXVA
on the decoder if possible, and drops optional Media Foundation transforms (MFTs) that do not support DXVA.

### -field MFTOPOLOGY_DXVA_NONE:1

The topology loader disables all video acceleration. This setting forces software processing, even when the decoder supports DXVA.

### -field MFTOPOLOGY_DXVA_FULL:2

The topology loader enables DXVA on every MFT that supports it.

## -remarks

This enumeration is used with the <a href="/windows/desktop/medfound/mf-topology-dxva-mode">MF_TOPOLOGY_DXVA_MODE</a> topology attribute.

If an MFT supports DXVA, the MFT must return <b>TRUE</b> for the <a href="/windows/desktop/medfound/mf-sa-d3d-aware-attribute">MF_SA_D3D_AWARE</a> attribute. To enable DXVA, the topology loader calls <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage">IMFTransform::ProcessMessage</a> on the MFT, passing the MFT a pointer to the <a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9">IDirect3DDeviceManager9</a> interface. The topology loader gets the <b>IDirect3DDeviceManager9</b> pointer from the media sink for the video stream. Typically the enhanced video renderer (EVR) is the media sink.

Previous versions of Microsoft Media Foundation supported DXVA only for decoders.

## -see-also

<a href="/windows/desktop/medfound/directx-video-acceleration-2-0">DirectX Video Acceleration 2.0</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
