---
UID: NF:d3d10.ID3D10Device.RSSetViewports
title: ID3D10Device::RSSetViewports
author: windows-sdk-content
description: Bind an array of viewports to the rasterizer stage of the pipeline.
old-location: direct3d10\id3d10device_rssetviewports.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_rssetviewports.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: 38205573-be63-f56a-8e33-466b9154f1a9, ID3D10Device interface [Direct3D 10],RSSetViewports method, ID3D10Device.RSSetViewports, ID3D10Device::RSSetViewports, RSSetViewports, RSSetViewports method [Direct3D 10], RSSetViewports method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::RSSetViewports, direct3d10.id3d10device_rssetviewports
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ID3D10Device.RSSetViewports
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10Device::RSSetViewports


## -description


Bind an array of <a href="https://msdn.microsoft.com/en-us/library/Bb205126(v=VS.85).aspx">viewports</a> to the <a href="https://msdn.microsoft.com/en-us/library/Bb205125(v=VS.85).aspx">rasterizer stage</a> of the pipeline.


## -parameters




### -param NumViewports [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of viewports to bind.


### -param pViewports [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Bb172500(v=VS.85).aspx">D3D10_VIEWPORT</a>*</b>

An array of viewports (see <a href="https://msdn.microsoft.com/en-us/library/Bb172500(v=VS.85).aspx">D3D10_VIEWPORT</a>) to bind to the device. Each viewport must have its extents within the allowed ranges: D3D10_VIEWPORT_BOUNDS_MIN, D3D10_VIEWPORT_BOUNDS_MAX, D3D10_MIN_DEPTH, and D3D10_MAX_DEPTH.


## -returns



This method does not return a value.




## -remarks



All viewports must be set atomically as one operation. Any viewports not defined by the call are disabled.

Which viewport to use is determined by the SV_ViewportArrayIndex semantic output by a geometry shader (see <a href="https://msdn.microsoft.com/en-us/library/Bb509647(v=VS.85).aspx">shader semantic syntax</a>). If a geometry shader does not make use of the SV_ViewportArrayIndex semantic then Direct3D will use the first viewport in the array.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

