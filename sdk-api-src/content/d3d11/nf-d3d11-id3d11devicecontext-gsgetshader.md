---
UID: NF:d3d11.ID3D11DeviceContext.GSGetShader
title: ID3D11DeviceContext::GSGetShader
author: windows-sdk-content
description: Get the geometry shader currently set on the device.
old-location: direct3d11\id3d11devicecontext_gsgetshader.htm
tech.root: direct3d11
ms.assetid: 5d5b935f-7eef-48ee-a2ed-82dd6c59aa19
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 154380d2-d835-0821-b4a5-1f810f07c0e3, GSGetShader, GSGetShader method [Direct3D 11], GSGetShader method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],GSGetShader method, ID3D11DeviceContext.GSGetShader, ID3D11DeviceContext::GSGetShader, d3d11/ID3D11DeviceContext::GSGetShader, direct3d11.id3d11devicecontext_gsgetshader
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.GSGetShader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d11.h
: 
- ID3D11DeviceContext.GSGetShader
: 
---

# ID3D11DeviceContext::GSGetShader


## -description


Get the geometry shader currently set on the device.


## -parameters




### -param ppGeometryShader [out]

Type: <b><a href="https://msdn.microsoft.com/c2b5863d-5773-4719-b1d0-2026f55fcef3">ID3D11GeometryShader</a>**</b>

Address of a pointer to a geometry shader (see <a href="https://msdn.microsoft.com/c2b5863d-5773-4719-b1d0-2026f55fcef3">ID3D11GeometryShader</a>) to be returned by the method.


### -param ppClassInstances [out, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476353(v=VS.85).aspx">ID3D11ClassInstance</a>**</b>

Pointer to an array of class instance interfaces (see <a href="https://msdn.microsoft.com/en-us/library/Ff476353(v=VS.85).aspx">ID3D11ClassInstance</a>).


### -param pNumClassInstances [in, out, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a>*</b>

The number of class-instance elements in the array.


## -returns



Returns nothing.




## -remarks



Any returned interfaces will have their reference count incremented by one. Applications should call IUnknown::Release on the returned interfaces when they are no longer needed to avoid memory leaks.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476385(v=VS.85).aspx">ID3D11DeviceContext</a>
 

 

