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

# IDirectInputEffectDriver::GetEffectStatus


## -description


The <b>IDirectInputEffectDriver::GetEffectStatus </b>method obtains information about the status of an effect. 


## -parameters




### -param






#### - dwEffect

Specifies the effect to be queried. 


#### - dwID

Indicates the external joystick number being addressed. 


#### - pdwStatus

Points to a <b>DWORD </b>that receives the effect status. The <b>DWORD</b> should be filled in with one of the following values: 





#### DIEGES_PLAYING

The effect is still playing. 



#### 0

The effect is not playing. 


## -returns



Returns S_OK if successful; otherwise, returns an error code.



