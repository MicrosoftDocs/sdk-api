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

# _WINBIO_ADAPTER_INTERFACE_VERSION structure


## -description


The <b>WINBIO_ADAPTER_INTERFACE_VERSION</b> structure contains a major and minor version number used in the engine, sensor, and storage adapter interface tables.


## -struct-fields




### -field MajorVersion

Contains the major version number.


### -field MinorVersion

Contains the minor version number.


## -remarks



This structure is used by the following structures:

<ul>
<li>
<a href="https://msdn.microsoft.com/04429f64-ae41-4c26-a777-bdb7aa92b685">WINBIO_ENGINE_INTERFACE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ab5a7146-936f-4ee5-9864-4f5a3b774724">WINBIO_SENSOR_INTERFACE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1cc7ce07-66df-43d9-9db2-50558a0f5f47">WINBIO_STORAGE_INTERFACE</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/5f04d912-f9bc-41d4-aa9e-b843e4b5a994">Plug-in Functions</a>



<a href="https://msdn.microsoft.com/64fb908c-72c2-4639-a2f6-77ede080512c">Plug-in Structures</a>
 

 

