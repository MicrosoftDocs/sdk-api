---
UID: NS:ddrawint._DD_FREEDRIVERMEMORYDATA
title: DD_FREEDRIVERMEMORYDATA (ddrawint.h)
author: windows-sdk-content
description: The DD_FREEDRIVERMEMORYDATA structure contains the details of the free request.
old-location: display\dd_freedrivermemorydata.htm
tech.root: display
ms.assetid: 48a42f19-bb4f-4325-b68b-91f59a674771
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PDD_FREEDRIVERMEMORYDATA, DD_FREEDRIVERMEMORYDATA, DD_FREEDRIVERMEMORYDATA structure [Display Devices], ddrawint/DD_FREEDRIVERMEMORYDATA, ddstrcts_a2d4a52f-25d5-4e02-8165-27ceadbddb36.xml, display.dd_freedrivermemorydata"
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
 - DD_FREEDRIVERMEMORYDATA
product: Windows
targetos: Windows
req.typenames: "*PDD_FREEDRIVERMEMORYDATA, DD_FREEDRIVERMEMORYDATA"
req.redist: 
ms.custom: 19H1
---

# DD_FREEDRIVERMEMORYDATA structure


## -description


The DD_FREEDRIVERMEMORYDATA structure contains the details of the free request.


## -struct-fields




### -field lpDD

Points to the <a href="https://msdn.microsoft.com/a59f064b-48cf-4491-82cd-84f59467af87">DD_DIRECTDRAW_GLOBAL</a> structure that describes the driver's device.


### -field lpDDSurface

Points to the <a href="https://msdn.microsoft.com/45a41cec-0257-4e26-809d-c2fc4c247328">DD_SURFACE_LOCAL</a> structure representing the surface that Microsoft DirectDraw is attempting to allocate.


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://msdn.microsoft.com/dd37c6b5-2039-487f-badc-840ac6cc7906">DdFreeDriverMemory</a> callback. A return code of DD_OK indicates that the driver succeeded in freeing some space; otherwise, the driver should set this to be DDERR_OUTOFMEMORY. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


### -field FreeDriverMemory

Used by the DirectDraw API and should not be filled in by the driver.


## -see-also




<a href="https://msdn.microsoft.com/dd37c6b5-2039-487f-badc-840ac6cc7906">DdFreeDriverMemory</a>
 

 

