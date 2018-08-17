---
UID: NF:d3d10effect.ID3D10StateBlock.ReleaseAllDeviceObjects
title: ID3D10StateBlock::ReleaseAllDeviceObjects
author: windows-sdk-content
description: Release all references to device objects.
old-location: direct3d10\id3d10stateblock_releasealldeviceobjects.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10stateblock_releasealldeviceobjects.htm
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: ID3D10StateBlock interface [Direct3D 10],ReleaseAllDeviceObjects method, ID3D10StateBlock.ReleaseAllDeviceObjects, ID3D10StateBlock::ReleaseAllDeviceObjects, ReleaseAllDeviceObjects, ReleaseAllDeviceObjects method [Direct3D 10], ReleaseAllDeviceObjects method [Direct3D 10],ID3D10StateBlock interface, d3d10effect/ID3D10StateBlock::ReleaseAllDeviceObjects, direct3d10.id3d10stateblock_releasealldeviceobjects, fbca6160-5745-e714-9c14-1caf025016ad
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10effect.h
req.include-header: 
req.redist: 
req.target-type: Windows
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
tech.root: 
req.typenames: D3D10_DEVICE_STATE_TYPES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10Effect.h
api_name:
 - ID3D10StateBlock.ReleaseAllDeviceObjects
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10StateBlock::ReleaseAllDeviceObjects


## -description


Release all references to device objects.


## -parameters






## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



Each time you return a pointer to an interface (by calling <a href="https://msdn.microsoft.com/08ac4a1f-b185-497f-88b2-e66268035dda">ID3D10StateBlock::GetDevice</a>), the internal reference count is incremented; when you are finished using a stateblock, call this method to release all references and avoid a memory leak.




## -see-also




<a href="https://msdn.microsoft.com/3705e8e6-f25f-4943-8c41-09fa6de02932">ID3D10StateBlock Interface</a>
 

 

