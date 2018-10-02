---
UID: NF:ddraw.IDirectDrawSurface7.GetAttachedSurface
title: IDirectDrawSurface7::GetAttachedSurface
author: windows-sdk-content
description: Obtains the attached surface that has the specified capabilities, and increments the reference count of the retrieved interface.
old-location: directdraw\idirectdrawsurface7_getattachedsurface.htm
tech.root: directdraw
ms.assetid: 0eae7e55-5ff7-41f6-ac6a-ce7fb6d809b9
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetAttachedSurface, GetAttachedSurface method [DirectDraw], GetAttachedSurface method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],GetAttachedSurface method, IDirectDrawSurface7.GetAttachedSurface, IDirectDrawSurface7::GetAttachedSurface, ddraw/IDirectDrawSurface7::GetAttachedSurface, directdraw.idirectdrawsurface7_getattachedsurface
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
 - IDirectDrawSurface7.GetAttachedSurface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectDrawSurface7::GetAttachedSurface


## -description


Obtains the attached surface that has the specified capabilities, and increments the reference count of the retrieved interface.


## -parameters




### -param arg1

TBD


### -param arg2

TBD




#### - lpDDSCaps [in]

A pointer to a <a href="https://msdn.microsoft.com/a2fd448c-0ae1-43cd-8561-77d537b741e7">DDSCAPS2</a> structure that indicates the hardware capabilities of the attached surface.


#### - lplpDDAttachedSurface [out]

A pointer to a variable to receive a pointer to the retrieved surface's <a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a> interface. The retrieved surface is the one that matches the description, according to the <i>lpDDSCaps</i> parameter.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_NOTFOUND</li>
<li>DDERR_SURFACELOST</li>
</ul>



## -remarks



Attachments are used to connect multiple DirectDrawSurface objects into complex structures, like the complex structures required to support 3-D page flipping with z-buffers. <b>GetAttachedSurface</b> fails if more than one surface is attached that matches the capabilities requested. In this case, the application must use the <a href="https://msdn.microsoft.com/7f8e9b53-3aff-491c-ab0c-2f414d1ddb27">IDirectDrawSurface7::EnumAttachedSurfaces</a> method to obtain the attached surfaces.



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>GetAttachedSurface</b> method.




## -see-also




<a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a>
 

 

