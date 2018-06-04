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

# D3D11_1_CREATE_DEVICE_CONTEXT_STATE_FLAG enumeration


## -description


Describes flags that are used to create a device context state object (<a href="https://msdn.microsoft.com/A8B9CADC-A9C7-4691-BB5C-3C12FF638C98">ID3DDeviceContextState</a>) with the <a href="https://msdn.microsoft.com/8887C3F1-3EA3-4948-A019-E3CB3F3D46C6">ID3D11Device1::CreateDeviceContextState</a> method.


## -enum-fields




### -field D3D11_1_CREATE_DEVICE_CONTEXT_STATE_SINGLETHREADED

You use this flag if your application will only call methods of Direct3D 11 and Direct3D 10 interfaces from a single thread. By default, Direct3D 11 and Direct3D 10 are  <a href="https://msdn.microsoft.com/0c4f984e-4dd0-4714-b911-592ca86d5dc0">thread-safe</a>. 
        By using this flag, you can increase performance. However, if you use this flag and your application calls methods from multiple threads, undefined behavior might result.


## -see-also




<a href="https://msdn.microsoft.com/1641713a-5ac8-4597-900b-1bba54f9f522">Core Enumerations</a>



<a href="https://msdn.microsoft.com/8887C3F1-3EA3-4948-A019-E3CB3F3D46C6">ID3D11Device1::CreateDeviceContextState</a>
 

 

