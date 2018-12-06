---
UID: NF:ddraw.IDirectDraw7.CreateSurface
title: IDirectDraw7::CreateSurface
author: windows-sdk-content
description: Creates a DirectDrawSurface object for this DirectDraw object.
old-location: directdraw\idirectdraw7_createsurface.htm
tech.root: directdraw
ms.assetid: 4f27e36f-d04f-43ce-9a3d-64c352c8f8d8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateSurface, CreateSurface method [DirectDraw], CreateSurface method [DirectDraw],IDirectDraw7 interface, IDirectDraw7 interface [DirectDraw],CreateSurface method, IDirectDraw7.CreateSurface, IDirectDraw7::CreateSurface, ddraw/IDirectDraw7::CreateSurface, directdraw.idirectdraw7_createsurface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ddraw.h
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
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ddraw.dll
api_name:
 - IDirectDraw7.CreateSurface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectDraw7::CreateSurface


## -description


Creates a DirectDrawSurface object for this DirectDraw object.



## -parameters




### -param arg1 [in]

Address of a <a href="https://msdn.microsoft.com/507c557f-eb3a-429c-a738-8d715e5d71d3">DDSURFACEDESC2</a> structure that describes the requested surface. Set any unused members of the <b>DDSURFACEDESC2</b> structure to 0 before calling this method. A <a href="https://msdn.microsoft.com/a2fd448c-0ae1-43cd-8561-77d537b741e7">DDSCAPS2</a> structure is a member of <b>DDSURFACEDESC2</b>.


### -param arg2 [out]

Address of a variable to be set to a valid <a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a> interface pointer if the call succeeds.


### -param arg3 [in]

Allows for future compatibility with COM aggregation features. Currently, this method returns an error if this parameter is not NULL.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INCOMPATIBLEPRIMARY</li>
<li>DDERR_INVALIDCAPS</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_INVALIDPIXELFORMAT</li>
<li>DDERR_NOALPHAHW</li>
<li>DDERR_NOCOOPERATIVELEVELSET</li>
<li>DDERR_NODIRECTDRAWHW</li>
<li>DDERR_NOEMULATION</li>
<li>DDERR_NOEXCLUSIVEMODE</li>
<li>DDERR_NOFLIPHW</li>
<li>DDERR_NOMIPMAPHW</li>
<li>DDERR_NOOVERLAYHW</li>
<li>DDERR_NOZBUFFERHW</li>
<li>DDERR_OUTOFMEMORY</li>
<li>DDERR_OUTOFVIDEOMEMORY</li>
<li>DDERR_PRIMARYSURFACEALREADYEXISTS</li>
<li>DDERR_UNSUPPORTEDMODE</li>
</ul>



## -remarks



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the <b>CreateSurface</b> method.




## -see-also




<a href="https://msdn.microsoft.com/1a1164fe-00c2-4469-8346-f86f7f48781e">IDirectDraw7</a>
 

 

