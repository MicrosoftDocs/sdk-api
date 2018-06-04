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

# IDirectManipulationPrimaryContent::SetSnapType


## -description


Specifies the type of snap point.


## -parameters




### -param motion [in]

One or more of the <a href="https://msdn.microsoft.com/a0b4da55-3ebb-4281-a372-4bc6b91e6789">DIRECTMANIPULATION_MOTION_TYPES</a> enumeration values.


### -param type [in]

One of the <a href="https://msdn.microsoft.com/4ba8c216-a5bb-409d-bce8-fc85023b63d9">DIRECTMANIPULATION_SNAPPOINT_TYPE</a> enumeration values.

If set to <b>DIRECTMANIPULATION_SNAPPOINT_TYPE_NONE</b>, snap points specified through <a href="https://msdn.microsoft.com/3257952d-903b-455c-9422-9739411a5924">SetSnapPoints</a> or <a href="https://msdn.microsoft.com/99d039fe-017a-47c5-95a1-5000efe92ba0">SetSnapInterval</a> are cleared.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/9910F5F5-950F-4099-9808-B46FA5BBA6FB">IDirectManipulationPrimaryContent</a>
 

 

