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

# PAC_CHANGES_CALLBACK_FN callback function


## -description


The <b>PAC_CHANGES_CALLBACK_FN</b>  function is used to add custom behavior to the app container change notification process.


## -parameters




### -param *context [in, optional]

Type: <b>void*</b>

Optional context pointer. It contains the value of the <i>context</i> parameter of the <a href="https://msdn.microsoft.com/2affb2a8-224c-4d2d-86e2-f194d3990dbe">NetworkIsolationRegisterForAppContainerChanges</a> function.


### -param *pChange [in]

Type: <b>const <a href="https://msdn.microsoft.com/b5f1b85d-3538-4be3-b97b-f9207cc7063b">INET_FIREWALL_AC_CHANGE</a>*</b>

The app container change information.


## -returns



This callback function does not return a value.




## -remarks



Call <a href="https://msdn.microsoft.com/2affb2a8-224c-4d2d-86e2-f194d3990dbe">NetworkIsolationRegisterForAppContainerChanges</a> to register this callback function.




## -see-also




<a href="https://msdn.microsoft.com/b5f1b85d-3538-4be3-b97b-f9207cc7063b">INET_FIREWALL_AC_CHANGE</a>



<a href="https://msdn.microsoft.com/2affb2a8-224c-4d2d-86e2-f194d3990dbe">NetworkIsolationRegisterForAppContainerChanges</a>
 

 

