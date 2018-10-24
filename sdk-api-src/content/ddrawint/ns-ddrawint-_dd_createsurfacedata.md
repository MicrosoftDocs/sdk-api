---
UID: NS:ddrawint._DD_CREATESURFACEDATA
title: "_DD_CREATESURFACEDATA"
author: windows-sdk-content
description: The DD_CREATESURFACEDATA structure contains information necessary to create a surface--in the case of CreateD3DBuffer, a command or vertex buffer.
old-location: display\dd_createsurfacedata.htm
tech.root: display
ms.assetid: 5a3b4267-43b4-44dc-abad-cb3f3d07f30e
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: "*PDD_CREATESURFACEDATA, DD_CREATESURFACEDATA, DD_CREATESURFACEDATA structure [Display Devices], _DD_CREATESURFACEDATA, ddrawint/DD_CREATESURFACEDATA, ddstrcts_bd51b416-f5b7-4a68-833b-7102de67488c.xml, display.dd_createsurfacedata"
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
 - DD_CREATESURFACEDATA
product: Windows
targetos: Windows
req.typenames: "*PDD_CREATESURFACEDATA, DD_CREATESURFACEDATA"
req.redist: 
---

# _DD_CREATESURFACEDATA structure


## -description


The DD_CREATESURFACEDATA structure contains information necessary to create a surface--in the case of <a href="https://msdn.microsoft.com/8b012e65-b78b-41a4-ac05-d9be015b6ed8">CreateD3DBuffer</a>, a command or vertex buffer.


## -struct-fields




### -field lpDD

Points to the <a href="https://msdn.microsoft.com/a59f064b-48cf-4491-82cd-84f59467af87">DD_DIRECTDRAW_GLOBAL</a> structure that describes the driver's device.


### -field lpDDSurfaceDesc

Points to the <a href="https://msdn.microsoft.com/d6656bae-9f90-497b-82d5-be4be3213687">DDSURFACEDESC</a> structure describing the surface or buffer that the driver should create.


### -field lplpSList

Points to a list of <a href="https://msdn.microsoft.com/45a41cec-0257-4e26-809d-c2fc4c247328">DD_SURFACE_LOCAL</a> structures describing the surface objects created by the driver. On Microsoft Windows 2000 and later, there is usually only one entry in this array. However, if the driver supports the Windows 98/Me-style surface creation techniques using <a href="https://msdn.microsoft.com/89a22163-a678-4c72-932a-ae4d17922e0b">DdGetDriverInfo</a> with GUID_NTPrivateDriverCaps, and the driver sets the DDHAL_PRIVATECAP_ATOMICSURFACECREATION flag, the member contains a list of surfaces (usually more than one). 


### -field dwSCnt

Specifies the number of surfaces in the list to which <b>lplpSList</b> points. This value is usually 1 on Windows 2000 and later. However, if the driver support the Windows 98/Me-style surface creation techniques using <a href="https://msdn.microsoft.com/89a22163-a678-4c72-932a-ae4d17922e0b">DdGetDriverInfo</a> with GUID_NTPrivateDriverCaps, the member contains the actual number of surfaces in the list (usually more than one). 


### -field ddRVal

Specifies the location in which the driver writes the return value of either the <a href="https://msdn.microsoft.com/45c793ed-34e8-4a15-91f4-9a258c1842fd">DdCreateSurface</a> or <a href="https://msdn.microsoft.com/8b012e65-b78b-41a4-ac05-d9be015b6ed8">CreateD3DBuffer</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


### -field CreateSurface

Used by the Microsoft DirectDraw API and should not be filled in by the driver.


## -see-also




<a href="https://msdn.microsoft.com/8b012e65-b78b-41a4-ac05-d9be015b6ed8">CreateD3DBuffer</a>



<a href="https://msdn.microsoft.com/45c793ed-34e8-4a15-91f4-9a258c1842fd">DdCreateSurface</a>



<a href="https://msdn.microsoft.com/89a22163-a678-4c72-932a-ae4d17922e0b">DdGetDriverInfo</a>
 

 

