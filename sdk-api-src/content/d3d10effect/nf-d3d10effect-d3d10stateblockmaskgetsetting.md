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

# D3D10StateBlockMaskGetSetting function


## -description


Get an element in a state-block mask; determine if an element is allowed by the mask for capturing and applying.


## -parameters




### -param pMask [in]

Type: <b><a href="https://msdn.microsoft.com/3188002c-a49f-4991-8fd5-75b31de8b790">D3D10_STATE_BLOCK_MASK</a>*</b>

State block mask. See <a href="https://msdn.microsoft.com/3188002c-a49f-4991-8fd5-75b31de8b790">D3D10_STATE_BLOCK_MASK</a>.


### -param StateType [in]

Type: <b><a href="https://msdn.microsoft.com/cc05f305-f93b-4f82-a554-708eb6643d32">D3D10_DEVICE_STATE_TYPES</a></b>

The type of device state. See <a href="https://msdn.microsoft.com/cc05f305-f93b-4f82-a554-708eb6643d32">D3D10_DEVICE_STATE_TYPES</a>.


### -param Entry [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The entry within the device state. This is only relevant for state types that have more than one entry, such as D3D10_DST_GS_SAMPLERS.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns true if the specified feature is allowed by the mask for capturing and applying, and false otherwise.




## -see-also




<a href="https://msdn.microsoft.com/012577cd-970e-43bc-996e-3be7c2283b60">Core Functions</a>



<a href="https://msdn.microsoft.com/b76643f0-387f-49c6-80e5-4d7b406b4db7">Effect Functions</a>
 

 

