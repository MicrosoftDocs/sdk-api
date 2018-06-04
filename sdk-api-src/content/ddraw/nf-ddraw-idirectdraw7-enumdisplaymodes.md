---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IDirectDraw7::EnumDisplayModes


## -description


Enumerates all the display modes that the hardware exposes through the DirectDraw object and that are compatible with a provided surface description.



## -parameters




### -param






#### - dwFlags [in]

This value consists of one or more of the following flags:



#### DDEDM_REFRESHRATES

Enumerates modes with different refresh rates. <b>IDirectDraw7::EnumDisplayModes</b> guarantees that a particular mode is enumerated only once. This flag specifies whether the refresh rate is taken into account when determining whether a mode is unique.



#### DDEDM_STANDARDVGAMODES

Enumerates Mode 13 in addition to the 320x200x8 Mode X mode.


#### - lpContext [in]

Address of an application-defined structure to be passed to each enumeration member.


#### - lpDDSurfaceDesc2 [in]

Address of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550340">DDSURFACEDESC2</a> structure to be checked against available modes. If the value of this parameter is NULL, all modes are enumerated.


#### - lpEnumModesCallback [in]

Address of the <a href="https://msdn.microsoft.com/53185A9A-EBA3-4443-8E76-AC85E69B39F2">EnumModesCallback2</a> function that the enumeration procedure calls every time a match is found.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
</ul>



## -remarks



<b>IDirectDraw7::EnumDisplayModes</b> enumerates the <b>dwRefreshRate</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550340">DDSURFACEDESC2</a> structure; the IDirectDraw::EnumDisplayModes method does not have this ability. If you use the <a href="https://msdn.microsoft.com/385918cd-64f1-449c-822a-0034a8184fb9">IDirectDraw7::SetDisplayMode</a> method to set the refresh rate of a new mode, use <b>IDirectDraw7::EnumDisplayModes</b> to enumerate the <b>dwRefreshRate</b> member.



<b>IDirectDraw7::EnumDisplayModes</b> differs from its counterparts in former interfaces in that it accepts the address of an <a href="https://msdn.microsoft.com/53185A9A-EBA3-4443-8E76-AC85E69B39F2">EnumModesCallback2</a> function as a parameter, rather than an <a href="https://msdn.microsoft.com/5959FD6F-7C48-43EA-8C7C-BCA659D06CE2">EnumModesCallback</a> function.



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the <b>IDirectDraw7::EnumDisplayModes</b> method.




## -see-also




<a href="https://msdn.microsoft.com/1a1164fe-00c2-4469-8346-f86f7f48781e">IDirectDraw7</a>
 

 

