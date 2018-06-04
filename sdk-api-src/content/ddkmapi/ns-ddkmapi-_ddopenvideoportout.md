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

# _DDOPENVIDEOPORTOUT structure


## -description


The DDOPENVIDEOPORTOUT structure contains a Microsoft DirectDraw return code and a new surface handle if <b>ddRVal</b> is set to DD_OK. This new handle must be used on all subsequent calls that require a <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a> object handle. 


## -struct-fields




### -field ddRVal

Specifies the location in which DirectDraw writes the return value of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff557364">DxApi</a> function for <a href="https://msdn.microsoft.com/library/windows/hardware/ff551498">DD_DXAPI_OPENVIDEOPORT</a> operations. A return code of DD_OK indicates success.


### -field hVideoPort

Handle to the new VPE object.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551498">DD_DXAPI_OPENVIDEOPORT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff557364">DxApi</a>
 

 

