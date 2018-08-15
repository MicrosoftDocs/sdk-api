---
UID: NF:d3d10.ID3D10Device.GSGetShader
title: ID3D10Device::GSGetShader
author: windows-sdk-content
description: Get the geometry shader currently set on the device.
old-location: direct3d10\id3d10device_gsgetshader.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_gsgetshader.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GSGetShader, GSGetShader method [Direct3D 10], GSGetShader method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],GSGetShader method, ID3D10Device.GSGetShader, ID3D10Device::GSGetShader, cdbac92b-f473-124b-66e8-4af3395c926a, d3d10/ID3D10Device::GSGetShader, direct3d10.id3d10device_gsgetshader
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10.h
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
 - ID3D10Device.GSGetShader
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::GSGetShader


## -description


Get the geometry shader currently set on the device.


## -parameters




### -param ppGeometryShader [out]

Type: <b><a href="https://msdn.microsoft.com/ffe713b9-93d6-4e0a-9cf6-014ac6b8a692">ID3D10GeometryShader</a>**</b>

Address of a pointer to a geometry shader (see <a href="https://msdn.microsoft.com/ffe713b9-93d6-4e0a-9cf6-014ac6b8a692">ID3D10GeometryShader</a>) to be returned by the method.


## -returns



Returns nothing.




## -remarks



Any returned interfaces will have their reference count incremented by one. Applications should call <a href="http://msdn.microsoft.com/en-us/library/ms682317(VS.85).aspx">IUnknown::Release</a> on the returned interfaces when they are no longer needed to avoid memory leaks.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

