---
UID: NF:d3d10.ID3D10Device.IAGetIndexBuffer
title: ID3D10Device::IAGetIndexBuffer
author: windows-sdk-content
description: Get a pointer to the index buffer that is bound to the input-assembler stage.
old-location: direct3d10\id3d10device_iagetindexbuffer.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_iagetindexbuffer.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAGetIndexBuffer, IAGetIndexBuffer method [Direct3D 10], IAGetIndexBuffer method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],IAGetIndexBuffer method, ID3D10Device.IAGetIndexBuffer, ID3D10Device::IAGetIndexBuffer, d3d10/ID3D10Device::IAGetIndexBuffer, direct3d10.id3d10device_iagetindexbuffer, ed98b873-1411-e17d-aa80-9545533db76a
ms.topic: method
req.header: d3d10.h
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.IAGetIndexBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10Device::IAGetIndexBuffer


## -description


Get a pointer to the <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">index buffer</a> that is bound to the <a href="https://msdn.microsoft.com/en-us/library/Bb205116(v=VS.85).aspx">input-assembler</a> stage.


## -parameters




### -param pIndexBuffer [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173510(v=VS.85).aspx">ID3D10Buffer</a>**</b>

A pointer to an index buffer returned by the method (see <a href="https://msdn.microsoft.com/en-us/library/Bb173510(v=VS.85).aspx">ID3D10Buffer</a>).


### -param Format [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a>*</b>

Specifies format of the data in the index buffer (see <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a>). These formats provide the size and type of the data in the buffer. The only formats allowed for index buffer data are 16-bit (DXGI_FORMAT_R16_UINT) and 32-bit (DXGI_FORMAT_R32_UINT) integers.


### -param Offset [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

Offset (in bytes) from the start of the index buffer, to the first index to use.


## -returns



Returns nothing.




## -remarks



Any returned interfaces will have their reference count incremented by one. Applications should call <a href="http://msdn.microsoft.com/en-us/library/ms682317(VS.85).aspx">IUnknown::Release</a> on the returned interfaces when they are no longer needed to avoid memory leaks.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

