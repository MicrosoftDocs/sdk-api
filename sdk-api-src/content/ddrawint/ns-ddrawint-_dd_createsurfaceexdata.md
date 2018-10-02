---
UID: NS:ddrawint._DD_CREATESURFACEEXDATA
title: "_DD_CREATESURFACEEXDATA"
author: windows-sdk-content
description: The DD_CREATESURFACEEXDATA structure contains information required for the driver to create a surface and associate with it a supplied texture handle.
old-location: display\dd_createsurfaceexdata.htm
tech.root: Display
ms.assetid: 61965d6b-7473-4121-8c85-fb677a665388
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PDD_CREATESURFACEEXDATA, DD_CREATESURFACEEXDATA, DD_CREATESURFACEEXDATA structure [Display Devices], _DD_CREATESURFACEEXDATA, d3dstrct_221c1055-03a3-4b43-bef4-8b0fbd6eb45e.xml, ddrawint/DD_CREATESURFACEEXDATA, display.dd_createsurfaceexdata"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ddrawint.h
req.include-header: Winddi.h
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
 - ddrawint.h
api_name:
 - DD_CREATESURFACEEXDATA
product: Windows
targetos: Windows
req.typenames: "*PDD_CREATESURFACEEXDATA, DD_CREATESURFACEEXDATA"
req.redist: 
---

# _DD_CREATESURFACEEXDATA structure


## -description


The DD_CREATESURFACEEXDATA structure contains information required for the driver to create a surface and associate with it a supplied texture handle.


## -struct-fields




### -field dwFlags

Specifies a set of flags for the <b>D3dCreateSurfaceEx</b> function that are currently not used and always zero.


### -field lpDDLcl

Specifies a handle to the DirectDraw object created by the application. This is the scope within which the <b>lpDDSLcl</b> handles exist. A <a href="https://msdn.microsoft.com/58e378b7-863a-46d4-91cb-904ed4e892a3">DD_DIRECTDRAW_LOCAL</a> structure describes the driver.


### -field lpDDSLcl

Specifies a handle to the DirectDraw surface to be created for Direct3D. These handles are unique within each different DD_DIRECTDRAW_LOCAL structure. A <a href="https://msdn.microsoft.com/45a41cec-0257-4e26-809d-c2fc4c247328">DD_SURFACE_LOCAL</a> structure represents the created surface object.


### -field ddRVal

Specifies the location where the driver writes the return value of the <a href="https://msdn.microsoft.com/dd07e49c-ec1f-4ba6-8b17-80ce6d3c5813">D3dCreateSurfaceEx</a> callback. A return code of D3D_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/033beb6e-5872-4cb3-8f39-459e2fff82cd">Return Codes for Direct3D Driver Callbacks</a>.


## -see-also




<a href="https://msdn.microsoft.com/dd07e49c-ec1f-4ba6-8b17-80ce6d3c5813">D3dCreateSurfaceEx</a>



<a href="https://msdn.microsoft.com/58e378b7-863a-46d4-91cb-904ed4e892a3">DD_DIRECTDRAW_LOCAL</a>



<a href="https://msdn.microsoft.com/45a41cec-0257-4e26-809d-c2fc4c247328">DD_SURFACE_LOCAL</a>
 

 

