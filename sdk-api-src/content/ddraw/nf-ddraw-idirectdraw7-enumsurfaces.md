---
UID: NF:ddraw.IDirectDraw7.EnumSurfaces
title: IDirectDraw7::EnumSurfaces
author: windows-sdk-content
description: Enumerates all the existing or possible surfaces that meet the specified surface description.
old-location: directdraw\idirectdraw7_enumsurfaces.htm
tech.root: directdraw
ms.assetid: d97135f3-9921-4e0c-b5ba-e4f709a5e32d
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: DDENUMSURFACES_ALL, DDENUMSURFACES_CANBECREATED, DDENUMSURFACES_DOESEXIST, DDENUMSURFACES_MATCH, DDENUMSURFACES_NOMATCH, EnumSurfaces, EnumSurfaces method [DirectDraw], EnumSurfaces method [DirectDraw],IDirectDraw7 interface, IDirectDraw7 interface [DirectDraw],EnumSurfaces method, IDirectDraw7.EnumSurfaces, IDirectDraw7::EnumSurfaces, ddraw/IDirectDraw7::EnumSurfaces, directdraw.idirectdraw7_enumsurfaces
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
 - IDirectDraw7.EnumSurfaces
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectDraw7::EnumSurfaces


## -description


Enumerates all the existing or possible surfaces that meet the specified surface description.



## -parameters




### -param arg1 [in]

A combination of one search type flag and one matching flag. The search type flag determines how the method searches for matching surfaces; you can search for surfaces that can be created using the description in the <i>lpDDSD2</i> parameter or for existing surfaces that already match that description. The matching flag determines whether the method enumerates all surfaces, only those that match, or only those that do not match the description in the <i>lpDDSD2</i> parameter.

<b>Search type flags</b>



#### DDENUMSURFACES_CANBECREATED

Enumerates the first surface that can be created and meets the search criterion. This flag can be used only with the DDENUMSURFACES_MATCH flag.



#### DDENUMSURFACES_DOESEXIST

Enumerates the already existing surfaces that meet the search criterion.

<b>Matching flags</b>



#### DDENUMSURFACES_ALL

Enumerates all surfaces that meet the search criterion. This flag can be used only with the DDENUMSURFACES_DOESEXIST search type flag.



#### DDENUMSURFACES_MATCH

Searches for any surface that matches the surface description.



#### DDENUMSURFACES_NOMATCH

Searches for any surface that does not match the surface description.


### -param arg2 [in]

Address of a <a href="https://msdn.microsoft.com/507c557f-eb3a-429c-a738-8d715e5d71d3">DDSURFACEDESC2</a> structure that defines the surface of interest. This parameter can be NULL if <i>dwFlags</i> includes the DDENUMSURFACES_ALL flag.


### -param arg3 [in]

Address of an application-defined structure to be passed to each enumeration member.


### -param arg4 [in]

Address of the <a href="https://msdn.microsoft.com/DA0FBED3-B61F-4CC3-9B6D-132A9F8ECFE0">EnumSurfacesCallback7</a> function that the enumeration procedure calls every time a match is found.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
</ul>



## -remarks



If the DDENUMSURFACES_CANBECREATED flag is set, this method attempts to temporarily create a surface that meets the search criterion.

When you use the DDENUMSURFACES_DOESEXIST flag, an enumerated surface's reference count is incremented—if you are not going to use the surface, be sure to use <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IDirectDrawSurface7::Release</a> to release it after each enumeration. If you will be using the surface, release it when it is no longer needed.



This method differs from its counterparts in previous interface versions in that it accepts a pointer to an <a href="https://msdn.microsoft.com/DA0FBED3-B61F-4CC3-9B6D-132A9F8ECFE0">EnumSurfacesCallback7</a> function, rather than an <a href="https://msdn.microsoft.com/4195C266-4F1D-4DD6-935E-78D07ACAA765">EnumSurfacesCallback</a> or <a href="https://msdn.microsoft.com/BC10A26B-50A3-48C5-94D7-B9C9E8FFE768">EnumSurfacesCallback2</a> function.



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>IDirectDraw7::EnumSurfaces</b> method.




## -see-also




<a href="https://msdn.microsoft.com/1a1164fe-00c2-4469-8346-f86f7f48781e">IDirectDraw7</a>
 

 

