---
UID: NF:d3d10effect.ID3D10StateBlock.Capture
title: ID3D10StateBlock::Capture
author: windows-sdk-content
description: Capture the current value of states that are included in a stateblock.
old-location: direct3d10\id3d10stateblock_capture.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10stateblock_capture.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: 9484ba4e-87ec-bd46-89ed-f4dc19c3d6e2, Capture, Capture method [Direct3D 10], Capture method [Direct3D 10],ID3D10StateBlock interface, ID3D10StateBlock interface [Direct3D 10],Capture method, ID3D10StateBlock.Capture, ID3D10StateBlock::Capture, d3d10effect/ID3D10StateBlock::Capture, direct3d10.id3d10stateblock_capture
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10effect.h
req.include-header: D3D10.h
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
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10StateBlock.Capture
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10StateBlock::Capture


## -description


Capture the current value of states that are included in a stateblock.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



Capture captures current values for states within an existing state block. It does not capture the entire state of the device. Creating an empty stateblock and calling Capture does nothing if no states have been set.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb173856(v=VS.85).aspx">ID3D10StateBlock Interface</a>
 

 

