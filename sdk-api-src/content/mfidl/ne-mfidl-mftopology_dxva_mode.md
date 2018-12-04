---
UID: NE:mfidl.MFTOPOLOGY_DXVA_MODE
title: MFTOPOLOGY_DXVA_MODE
author: windows-sdk-content
description: Specifies whether the topology loader enables Microsoft DirectX Video Acceleration (DXVA) in the topology.
old-location: mf\mftopology_dxva_mode.htm
tech.root: medfound
ms.assetid: c47f505a-1b98-4309-b462-5b911e1f591f
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: MFTOPOLOGY_DXVA_DEFAULT, MFTOPOLOGY_DXVA_FULL, MFTOPOLOGY_DXVA_MODE, MFTOPOLOGY_DXVA_MODE enumeration [Media Foundation], MFTOPOLOGY_DXVA_NONE, mf.mftopology_dxva_mode, mfidl/MFTOPOLOGY_DXVA_DEFAULT, mfidl/MFTOPOLOGY_DXVA_FULL, mfidl/MFTOPOLOGY_DXVA_MODE, mfidl/MFTOPOLOGY_DXVA_NONE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MFTOPOLOGY_DXVA_MODE
product: Windows
targetos: Windows
req.typenames: MFTOPOLOGY_DXVA_MODE
req.redist: 
---

# MFTOPOLOGY_DXVA_MODE enumeration


## -description


Specifies whether the topology loader enables Microsoft DirectX Video Acceleration (DXVA) in the topology.


## -enum-fields




### -field MFTOPOLOGY_DXVA_DEFAULT

The topology loader enables DXVA
on the decoder if possible, and drops optional Media Foundation transforms (MFTs) that do not support DXVA.


### -field MFTOPOLOGY_DXVA_NONE

The topology loader disables all video acceleration. This setting forces software processing, even when the decoder supports DXVA.


### -field MFTOPOLOGY_DXVA_FULL

The topology loader enables DXVA on every MFT that supports it.


## -remarks



This enumeration is used with the <a href="https://msdn.microsoft.com/03783ef3-f957-41e3-9734-94cb34ecc088">MF_TOPOLOGY_DXVA_MODE</a> topology attribute.

If an MFT supports DXVA, the MFT must return <b>TRUE</b> for the <a href="https://msdn.microsoft.com/db6a8b20-fda0-4ffe-b1b5-a77b7604d290">MF_SA_D3D_AWARE</a> attribute. To enable DXVA, the topology loader calls <a href="https://msdn.microsoft.com/a6dc67e5-8473-444a-8463-24f411e59565">IMFTransform::ProcessMessage</a> on the MFT, passing the MFT a pointer to the <a href="https://msdn.microsoft.com/e661e666-dc51-4a71-9ecd-62a667bb217d">IDirect3DDeviceManager9</a> interface. The topology loader gets the <b>IDirect3DDeviceManager9</b> pointer from the media sink for the video stream. Typically the enhanced video renderer (EVR) is the media sink.

Previous versions of Microsoft Media Foundation supported DXVA only for decoders.




## -see-also




<a href="https://msdn.microsoft.com/acb73b20-89fa-4a48-be4a-846715a239b0">DirectX Video Acceleration 2.0</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

