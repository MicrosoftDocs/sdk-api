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

# HueSaturationLightness::SetParameters


## -description


The <b>HueSaturationLightness::SetParameters</b> method sets the parameters of this <a href="https://msdn.microsoft.com/3bb652eb-62f0-4948-9484-4439dc9bd54e">HueSaturationLightness</a> object. 


## -parameters




### -param parameters [in]

Type: <b>const <a href="https://msdn.microsoft.com/d46ef884-ac73-4fa0-8c4d-d033ac1ed406">HueSaturationLightnessParams</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/d46ef884-ac73-4fa0-8c4d-d033ac1ed406">HueSaturationLightnessParams</a> structure that specifies the parameters.


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/3bb652eb-62f0-4948-9484-4439dc9bd54e">HueSaturationLightness</a>



<a href="https://msdn.microsoft.com/a743d9fb-ba19-4dfd-be66-2339ce27d70c">HueSaturationLightness::GetParameters</a>
 

 

