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

# ICOMAdminCatalog::GetEventClassesForIID


## -description


Retrieves a list of the event classes registered on the computer that implement a specified interface.


## -parameters




### -param bstrIID [in]

A GUID representing the interface for which event classes should be found. If this parameter is <b>NULL</b>, the method retrieves all event classes registered on the computer.


### -param ppsaVarCLSIDs [out]

An array of CLSIDs for the event classes implementing the interface specified in <i>bstrIID</i>.


### -param ppsaVarProgIDs [out]

An array of ProgIDs for the event classes implementing the interface specified in <i>bstrIID</i>.


### -param ppsaVarDescriptions [out]

An array of descriptions for the event classes implementing the interface specified in <i>bstrIID</i>.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/2c3c49df-9ca5-40ea-b45c-f4eca1004602">ICOMAdminCatalog</a>
 

 

