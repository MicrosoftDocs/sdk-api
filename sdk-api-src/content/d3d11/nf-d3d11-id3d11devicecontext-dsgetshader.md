---
UID: NF:d3d11.ID3D11DeviceContext.DSGetShader
title: ID3D11DeviceContext::DSGetShader
author: windows-sdk-content
description: Get the domain shader currently set on the device.
old-location: direct3d11\id3d11devicecontext_dsgetshader.htm
tech.root: direct3d11
ms.assetid: b04a9640-e28e-419e-9a8c-02685e7a0883
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: 23ad23d5-5ea9-e2f1-ce64-770b35bc0586, DSGetShader, DSGetShader method [Direct3D 11], DSGetShader method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],DSGetShader method, ID3D11DeviceContext.DSGetShader, ID3D11DeviceContext::DSGetShader, d3d11/ID3D11DeviceContext::DSGetShader, direct3d11.id3d11devicecontext_dsgetshader
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
 - ID3D11DeviceContext.DSGetShader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11DeviceContext::DSGetShader


## -description


Get the domain shader currently set on the device.


## -parameters




### -param ppDomainShader [out]

Type: <b><a href="https://msdn.microsoft.com/cd01c872-4df5-4741-90c5-211d3e393f89">ID3D11DomainShader</a>**</b>

Address of a pointer to a domain shader (see <a href="https://msdn.microsoft.com/cd01c872-4df5-4741-90c5-211d3e393f89">ID3D11DomainShader</a>) to be returned by the method.


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
 

 

