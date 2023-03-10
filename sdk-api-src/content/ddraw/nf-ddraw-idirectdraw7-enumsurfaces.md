---
UID: NF:ddraw.IDirectDraw7.EnumSurfaces
title: IDirectDraw7::EnumSurfaces (ddraw.h)
description: Enumerates all the existing or possible surfaces that meet the specified surface description.
helpviewer_keywords: ["DDENUMSURFACES_ALL","DDENUMSURFACES_CANBECREATED","DDENUMSURFACES_DOESEXIST","DDENUMSURFACES_MATCH","DDENUMSURFACES_NOMATCH","EnumSurfaces","EnumSurfaces method [DirectDraw]","EnumSurfaces method [DirectDraw]","IDirectDraw7 interface","IDirectDraw7 interface [DirectDraw]","EnumSurfaces method","IDirectDraw7.EnumSurfaces","IDirectDraw7::EnumSurfaces","ddraw/IDirectDraw7::EnumSurfaces","directdraw.idirectdraw7_enumsurfaces"]
old-location: directdraw\idirectdraw7_enumsurfaces.htm
tech.root: directdraw
ms.assetid: d97135f3-9921-4e0c-b5ba-e4f709a5e32d
ms.date: 12/05/2018
ms.keywords: DDENUMSURFACES_ALL, DDENUMSURFACES_CANBECREATED, DDENUMSURFACES_DOESEXIST, DDENUMSURFACES_MATCH, DDENUMSURFACES_NOMATCH, EnumSurfaces, EnumSurfaces method [DirectDraw], EnumSurfaces method [DirectDraw],IDirectDraw7 interface, IDirectDraw7 interface [DirectDraw],EnumSurfaces method, IDirectDraw7.EnumSurfaces, IDirectDraw7::EnumSurfaces, ddraw/IDirectDraw7::EnumSurfaces, directdraw.idirectdraw7_enumsurfaces
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectDraw7::EnumSurfaces
 - ddraw/IDirectDraw7::EnumSurfaces
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ddraw.dll
api_name:
 - IDirectDraw7.EnumSurfaces
---

# IDirectDraw7::EnumSurfaces


## -description

Enumerates all the existing or possible surfaces that meet the specified surface description.

## -parameters

### -param unnamedParam1 [in]

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

### -param unnamedParam2 [in]

Address of a <a href="/previous-versions/windows/hardware/drivers/ff550340(v=vs.85)">DDSURFACEDESC2</a> structure that defines the surface of interest. This parameter can be NULL if <i>dwFlags</i> includes the DDENUMSURFACES_ALL flag.

### -param unnamedParam3 [in]

Address of an application-defined structure to be passed to each enumeration member.

### -param unnamedParam4 [in]

Address of the <a href="/windows/desktop/api/ddraw/nc-ddraw-lpddenumsurfacescallback7">EnumSurfacesCallback7</a> function that the enumeration procedure calls every time a match is found.

## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
</ul>

## -remarks

If the DDENUMSURFACES_CANBECREATED flag is set, this method attempts to temporarily create a surface that meets the search criterion.

When you use the DDENUMSURFACES_DOESEXIST flag, an enumerated surface's reference count is incremented—if you are not going to use the surface, be sure to use <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IDirectDrawSurface7::Release</a> to release it after each enumeration. If you will be using the surface, release it when it is no longer needed.



This method differs from its counterparts in previous interface versions in that it accepts a pointer to an <a href="/windows/desktop/api/ddraw/nc-ddraw-lpddenumsurfacescallback7">EnumSurfacesCallback7</a> function, rather than an <a href="/windows/desktop/api/ddraw/nc-ddraw-lpddenumsurfacescallback">EnumSurfacesCallback</a> or <a href="/windows/desktop/api/ddraw/nc-ddraw-lpddenumsurfacescallback2">EnumSurfacesCallback2</a> function.





## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdraw7">IDirectDraw7</a>