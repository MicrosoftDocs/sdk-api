---
UID: NF:d3d10effect.ID3D10StateBlock.ReleaseAllDeviceObjects
title: ID3D10StateBlock::ReleaseAllDeviceObjects (d3d10effect.h)
author: windows-sdk-content
description: Release all references to device objects.
old-location: direct3d10\id3d10stateblock_releasealldeviceobjects.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10stateblock_releasealldeviceobjects.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D10StateBlock interface [Direct3D 10],ReleaseAllDeviceObjects method, ID3D10StateBlock.ReleaseAllDeviceObjects, ID3D10StateBlock::ReleaseAllDeviceObjects, ReleaseAllDeviceObjects, ReleaseAllDeviceObjects method [Direct3D 10], ReleaseAllDeviceObjects method [Direct3D 10],ID3D10StateBlock interface, d3d10effect/ID3D10StateBlock::ReleaseAllDeviceObjects, direct3d10.id3d10stateblock_releasealldeviceobjects, fbca6160-5745-e714-9c14-1caf025016ad
ms.topic: method
f1_keywords: ["d3d10effect/ID3D10StateBlock.ReleaseAllDeviceObjects"]
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
ms.custom: 19H1
---

# ID3D10StateBlock::ReleaseAllDeviceObjects


## -description


Release all references to device objects.


## -parameters






## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

Returns one of the following <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.




## -remarks



Each time you return a pointer to an interface (by calling <a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10stateblock-getdevice">ID3D10StateBlock::GetDevice</a>), the internal reference count is incremented; when you are finished using a stateblock, call this method to release all references and avoid a memory leak.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10stateblock">ID3D10StateBlock Interface</a>
 

 

