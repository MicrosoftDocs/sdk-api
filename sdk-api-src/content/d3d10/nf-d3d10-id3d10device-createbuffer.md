---
UID: NF:d3d10.ID3D10Device.CreateBuffer
title: ID3D10Device::CreateBuffer (d3d10.h)
author: windows-sdk-content
description: Create a buffer (vertex buffer, index buffer, or shader-constant buffer).
old-location: direct3d10\id3d10device_createbuffer.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_createbuffer.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateBuffer, CreateBuffer method [Direct3D 10], CreateBuffer method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],CreateBuffer method, ID3D10Device.CreateBuffer, ID3D10Device::CreateBuffer, d3d10/ID3D10Device::CreateBuffer, direct3d10.id3d10device_createbuffer, f67833a5-95f8-0430-5015-e074533c6dd1
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
 - ID3D10Device.CreateBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10Device::CreateBuffer


## -description


Create a <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">buffer</a> (vertex buffer, index buffer, or shader-constant buffer).


## -parameters




### -param pDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Bb204896(v=VS.85).aspx">D3D10_BUFFER_DESC</a>*</b>

Pointer to a buffer description (see <a href="https://msdn.microsoft.com/en-us/library/Bb204896(v=VS.85).aspx">D3D10_BUFFER_DESC</a>).


### -param pInitialData [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Bb172456(v=VS.85).aspx">D3D10_SUBRESOURCE_DATA</a>*</b>

Pointer to the initialization data (see <a href="https://msdn.microsoft.com/en-us/library/Bb172456(v=VS.85).aspx">D3D10_SUBRESOURCE_DATA</a>); use <b>NULL</b> to allocate space only.


### -param ppBuffer [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173510(v=VS.85).aspx">ID3D10Buffer</a>**</b>

Address of a pointer to the buffer created (see <a href="https://msdn.microsoft.com/en-us/library/Bb173510(v=VS.85).aspx">ID3D10Buffer Interface</a>). Set this parameter to <b>NULL</b> to validate the other input parameters (S_FALSE indicates a pass).


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



For example code, see:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb205130(v=VS.85).aspx">Create a Vertex Buffer</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb205130(v=VS.85).aspx">Create an Index Buffer</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

