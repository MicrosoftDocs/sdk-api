---
UID: NS:ddkmapi._DDOPENSURFACEIN
title: "_DDOPENSURFACEIN"
author: windows-sdk-content
description: The DDOPENSURFACEIN structure contains the DirectDrawSurface object information.
old-location: display\ddopensurfacein.htm
tech.root: display
ms.assetid: 98a5d436-096d-4698-8f2c-31a0455300ff
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: "*LPDDOPENSURFACEIN, DDOPENSURFACEIN, DDOPENSURFACEIN structure [Display Devices], LPDDOPENSURFACEIN, LPDDOPENSURFACEIN structure pointer [Display Devices], _DDOPENSURFACEIN, ddkmapi/DDOPENSURFACEIN, ddkmapi/LPDDOPENSURFACEIN, ddstrcts_406539e4-c43f-4871-b00b-30c71433d1fd.xml, display.ddopensurfacein"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ddkmapi.h
req.include-header: Ddkmapi.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddkmapi.h
api_name:
 - DDOPENSURFACEIN
product: Windows
targetos: Windows
req.typenames: DDOPENSURFACEIN, *LPDDOPENSURFACEIN
req.redist: 
---

# _DDOPENSURFACEIN structure


## -description


The DDOPENSURFACEIN structure contains the DirectDrawSurface object information. 


## -struct-fields




### -field hDirectDraw

Specifies the Microsoft DirectDraw object to which the surface handle is associated.


### -field dwSurfaceHandle

Specifies the DirectDrawSurface handle passed down from user mode.


### -field pfnSurfaceClose

Points to a <a href="https://msdn.microsoft.com/ee581d7b-c3b8-47e5-bae8-348b22ea0f95">pfnSurfaceClose</a> callback function that is called when the surface becomes unusable.


### -field pContext

Contains a value that is passed if the <b>pfnSurfaceClose</b> callback function is ever called.


## -see-also




<a href="https://msdn.microsoft.com/b2449bf4-d7ef-440e-ae1f-6ede2895b831">DD_DXAPI_OPENSURFACE</a>



<a href="https://msdn.microsoft.com/c4b38376-b54f-4fbb-b305-5951a1ea76a1">DxApi</a>
 

 

