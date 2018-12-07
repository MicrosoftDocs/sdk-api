---
UID: NF:d3d10effect.ID3D10StateBlock.ReleaseAllDeviceObjects
title: ID3D10StateBlock::ReleaseAllDeviceObjects
author: windows-sdk-content
description: Release all references to device objects.
old-location: direct3d10\id3d10stateblock_releasealldeviceobjects.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10stateblock_releasealldeviceobjects.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3D10StateBlock interface [Direct3D 10],ReleaseAllDeviceObjects method, ID3D10StateBlock.ReleaseAllDeviceObjects, ID3D10StateBlock::ReleaseAllDeviceObjects, ReleaseAllDeviceObjects, ReleaseAllDeviceObjects method [Direct3D 10], ReleaseAllDeviceObjects method [Direct3D 10],ID3D10StateBlock interface, d3d10effect/ID3D10StateBlock::ReleaseAllDeviceObjects, direct3d10.id3d10stateblock_releasealldeviceobjects, fbca6160-5745-e714-9c14-1caf025016ad
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d10effect.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
---

# ID3D10StateBlock::ReleaseAllDeviceObjects


## -description


Release all references to device objects.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



Each time you return a pointer to an interface (by calling <a href="https://msdn.microsoft.com/en-us/library/Bb173859(v=VS.85).aspx">ID3D10StateBlock::GetDevice</a>), the internal reference count is incremented; when you are finished using a stateblock, call this method to release all references and avoid a memory leak.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173856(v=VS.85).aspx">ID3D10StateBlock Interface</a>
 

 

