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

# RoRevokeActivationFactories function


## -description


Removes an array of registered activation factories from the Windows Runtime.


## -parameters




### -param cookie [in]

Type: <b><a href="https://msdn.microsoft.com/D74E5886-45DB-40DE-9740-D14341E78713">RO_REGISTRATION_COOKIE</a></b>


## -returns



This function does not return a value.




## -remarks



Call the <b>RoRevokeActivationFactories</b> function remove the activation factories represented in the  <i>cookie</i> array from the Windows Runtime.




## -see-also




<a href="https://msdn.microsoft.com/D74E5886-45DB-40DE-9740-D14341E78713">RO_REGISTRATION_COOKIE</a>



<a href="https://msdn.microsoft.com/527A7FF7-749D-4178-A397-5C538F6031F8">RoInitialize</a>



<a href="https://msdn.microsoft.com/8213f5de-3b1c-44c3-ad37-b2ebac8dbcd8">RoRegisterActivationFactories</a>
 

 

