---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

