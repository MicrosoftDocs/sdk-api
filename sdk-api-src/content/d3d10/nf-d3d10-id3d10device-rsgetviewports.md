---
UID: NF:d3d10.ID3D10Device.RSGetViewports
title: ID3D10Device::RSGetViewports
author: windows-sdk-content
description: Get the array of viewports bound to the rasterizer stage
old-location: direct3d10\id3d10device_rsgetviewports.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_rsgetviewports.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: ID3D10Device interface [Direct3D 10],RSGetViewports method, ID3D10Device.RSGetViewports, ID3D10Device::RSGetViewports, RSGetViewports, RSGetViewports method [Direct3D 10], RSGetViewports method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::RSGetViewports, d9ea7cbf-16e9-686e-f682-4c7619caae2c, direct3d10.id3d10device_rsgetviewports
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D10_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.RSGetViewports
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::RSGetViewports


## -description


Get the array of <a href="https://msdn.microsoft.com/library/Bb205126(v=VS.85).aspx">viewports</a> bound 
    to the <a href="https://msdn.microsoft.com/library/Bb205125(v=VS.85).aspx">rasterizer stage</a>



## -parameters




### -param NumViewports [in, out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

Number of viewports in <i>pViewports</i>.  
        If <i>pViewports</i> is <b>NULL</b>, this will be filled with the number of viewports currently bound.


### -param pViewports [out]

Type: <b><a href="https://msdn.microsoft.com/library/Bb172500(v=VS.85).aspx">D3D10_VIEWPORT</a>*</b>

An array of viewports (see <a href="https://msdn.microsoft.com/library/Bb172500(v=VS.85).aspx">D3D10_VIEWPORT</a>) to be filled with information from the device. If NumViewports is greater than 
        the actual number of viewports currently bound, then unused members of the array will contain 0.


## -returns



Returns nothing.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

