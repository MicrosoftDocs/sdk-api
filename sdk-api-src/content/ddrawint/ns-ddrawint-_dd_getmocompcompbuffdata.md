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

# _DD_GETMOCOMPCOMPBUFFDATA structure


## -description


The DD_GETMOCOMPCOMPBUFFDATA structure contains the compressed buffer information. 


## -struct-fields




### -field lpDD

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550595">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.


### -field lpGuid

Points to a GUID for which the compressed buffer information is requested. 


### -field dwWidth

Indicates the width in pixels of the uncompressed output frame.


### -field dwHeight

Indicates the height in pixels of the uncompressed output frame.


### -field ddPixelFormat

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550274">DDPIXELFORMAT</a> structure that contains the pixel format of the uncompressed output frame.


### -field dwNumTypesCompBuffs

Indicates how many different types of surfaces the driver requires to perform motion compensation using the requested GUID. 


### -field lpCompBuffInfo

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff549240">DDCOMPBUFFERINFO</a> structure that contains the driver-supplied information for each type of required surface. 


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://msdn.microsoft.com/7303f80d-1b6e-401f-a9ef-cf646b716c70">DdMoCompGetBuffInfo</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


## -see-also




<a href="https://msdn.microsoft.com/7303f80d-1b6e-401f-a9ef-cf646b716c70">DdMoCompGetBuffInfo</a>
 

 

