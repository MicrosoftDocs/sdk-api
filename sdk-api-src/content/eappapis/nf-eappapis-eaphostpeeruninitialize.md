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

# EapHostPeerUninitialize function


## -description


Uninitializes all  EAPHost authentication sessions. 

The <b>EapHostPeerUninitialize</b> function must be called after you are finished calling EAPHost supplicant run-time functions. In addition, if any re-authentication is expected for any reason it is best to call <b>EapHostPeerUninitialize</b>.


## -parameters






## -returns



This function does not return a value.




## -remarks




<a href="https://msdn.microsoft.com/4af7103e-85c8-472e-96fe-407f07a1f447">EapHostPeerInitialize</a> and <b>EapHostPeerUninitialize</b> are always thread
safe.

<b>EapHostPeerUninitialize</b> calls <b>CoUninitialize</b>.




## -see-also




<a href="https://msdn.microsoft.com/b1c473ba-9a12-4929-b4d0-27262117e9c0">EAPHost Supplicant Run-time Functions</a>



<a href="https://msdn.microsoft.com/4af7103e-85c8-472e-96fe-407f07a1f447">EapHostPeerInitialize</a>
 

 

