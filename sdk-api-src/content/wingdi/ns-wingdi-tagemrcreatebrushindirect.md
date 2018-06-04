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

# tagEMRCREATEBRUSHINDIRECT structure


## -description



The <b>EMRCREATEBRUSHINDIRECT</b> structure contains members for the <a href="https://msdn.microsoft.com/75f94ad1-ca25-4ad1-9e8c-ad1a4b8475a7">CreateBrushIndirect</a> enhanced metafile record.




## -struct-fields




### -field emr

The base structure for all record types.


### -field ihBrush

Index of brush in handle table.


### -field lb


            A <a href="https://msdn.microsoft.com/8e2053a9-d7b6-4bf7-b915-4c3871a46b37">LOGBRUSH32</a> structure containing information about the brush. The <b>lbStyle</b> member must be either the BS_SOLID, BS_HOLLOW, BS_NULL, or BS_HATCHED value.

Note, that if your code is used on both 32-bit and 64-bit platforms, you must use the <a href="https://msdn.microsoft.com/8e2053a9-d7b6-4bf7-b915-4c3871a46b37">LOGBRUSH32</a> structure. This maintains compatibility between the platforms when you record the metafile on one platform and use it on the other platform. If your code remains on one platform, it is sufficient to use <a href="https://msdn.microsoft.com/ded2c7a4-2248-4d01-95c6-ab4050719094">LOGBRUSH</a>.


## -see-also




<a href="https://msdn.microsoft.com/75f94ad1-ca25-4ad1-9e8c-ad1a4b8475a7">CreateBrushIndirect</a>



<a href="https://msdn.microsoft.com/ded2c7a4-2248-4d01-95c6-ab4050719094">LOGBRUSH</a>



<a href="https://msdn.microsoft.com/8e2053a9-d7b6-4bf7-b915-4c3871a46b37">LOGBRUSH32</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>
 

 

