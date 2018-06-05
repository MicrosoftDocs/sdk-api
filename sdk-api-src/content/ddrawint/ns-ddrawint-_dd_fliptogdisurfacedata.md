---
UID: NS:ddrawint._DD_FLIPTOGDISURFACEDATA
title: "_DD_FLIPTOGDISURFACEDATA"
author: windows-sdk-content
description: The DD_FLIPTOGDISURFACEDATA structure contains the GDI surface notification information.
old-location: display\dd_fliptogdisurfacedata.htm
old-project: display
ms.assetid: ac0fdaf7-0cb2-4474-b3dd-a039161513a4
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: "*PDD_FLIPTOGDISURFACEDATA, DD_FLIPTOGDISURFACEDATA, DD_FLIPTOGDISURFACEDATA structure [Display Devices], _DD_FLIPTOGDISURFACEDATA, ddrawint/DD_FLIPTOGDISURFACEDATA, ddstrcts_7e93a017-4f74-43c9-9aaa-6e64da35870d.xml, display.dd_fliptogdisurfacedata"
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
tech.root: 
req.typenames: "*PDD_FLIPTOGDISURFACEDATA, DD_FLIPTOGDISURFACEDATA"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ddrawint.h
api_name:
-	DD_FLIPTOGDISURFACEDATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DD_FLIPTOGDISURFACEDATA structure


## -description


The DD_FLIPTOGDISURFACEDATA structure contains the GDI surface notification information.


## -struct-fields




### -field lpDD

Points to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550586">DD_DIRECTDRAW_GLOBAL</a> structure that describes the driver's device.


### -field dwToGDI

Indicates that Microsoft DirectDraw is flipping to a GDI surface when <b>TRUE</b>; indicates that DirectDraw is flipping from a GDI surface when <b>FALSE</b>.


### -field dwReserved

Reserved for system use and should be ignored by the driver.


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://msdn.microsoft.com/279987bb-1697-4157-9d61-d503b0183e84">DdFlipToGDISurface</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


### -field FlipToGDISurface

Used by the DirectDraw API and should not be filled in by the driver.


## -see-also




<a href="https://msdn.microsoft.com/279987bb-1697-4157-9d61-d503b0183e84">DdFlipToGDISurface</a>
 

 

