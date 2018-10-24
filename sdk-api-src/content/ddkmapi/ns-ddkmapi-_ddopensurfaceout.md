---
UID: NS:ddkmapi._DDOPENSURFACEOUT
title: "_DDOPENSURFACEOUT"
author: windows-sdk-content
description: The DDOPENSURFACEOUT structure contains a new DirectDrawSurface handle, if the ddRVal member of DDOPENSURFACEOUT is set to DD_OK. This new handle must be used on all subsequent calls that require a DirectDrawSurface handle.
old-location: display\ddopensurfaceout.htm
tech.root: display
ms.assetid: 0cf0db38-f512-4ca1-a386-5544a1c9433e
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: "*LPDDOPENSURFACEOUT, DDOPENSURFACEOUT, DDOPENSURFACEOUT structure [Display Devices], LPDDOPENSURFACEOUT, LPDDOPENSURFACEOUT structure pointer [Display Devices], _DDOPENSURFACEOUT, ddkmapi/DDOPENSURFACEOUT, ddkmapi/LPDDOPENSURFACEOUT, ddstrcts_911314a4-692d-4909-9c30-e868a767e031.xml, display.ddopensurfaceout"
ms.prod: windows
ms.technology: windows-sdk
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
 - DDOPENSURFACEOUT
product: Windows
targetos: Windows
req.typenames: DDOPENSURFACEOUT, *LPDDOPENSURFACEOUT
req.redist: 
---

# _DDOPENSURFACEOUT structure


## -description


The DDOPENSURFACEOUT structure contains a new DirectDrawSurface handle, if the <b>ddRVal</b> member of DDOPENSURFACEOUT is set to DD_OK. This new handle must be used on all subsequent calls that require a DirectDrawSurface handle. 


## -struct-fields




### -field ddRVal

Specifies the location in which Microsoft DirectDraw writes the return value of the <a href="https://msdn.microsoft.com/c4b38376-b54f-4fbb-b305-5951a1ea76a1">DxApi</a> function for <a href="https://msdn.microsoft.com/b2449bf4-d7ef-440e-ae1f-6ede2895b831">DD_DXAPI_OPENSURFACE</a> operations. A return code of DD_OK indicates success.


### -field hSurface

Handle to the new DirectDrawSurface object.


## -see-also




<a href="https://msdn.microsoft.com/b2449bf4-d7ef-440e-ae1f-6ede2895b831">DD_DXAPI_OPENSURFACE</a>



<a href="https://msdn.microsoft.com/c4b38376-b54f-4fbb-b305-5951a1ea76a1">DxApi</a>
 

 

