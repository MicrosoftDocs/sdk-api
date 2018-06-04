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

# _EAP_METHOD_INFO_ARRAY_EX structure


## -description


The <b>EAP_METHOD_INFO_ARRAY_EX</b> structure contains information about all of the EAP methods installed on the client computer. After populating <b>EAP_METHOD_INFO_ARRAY_EX</b>, EAPHost passes this method information to the supplicant.


## -struct-fields




### -field dwNumberOfMethods

The number of <a href="https://msdn.microsoft.com/2d25f418-2130-4f9c-b3f4-f639dfba020a">EAP_METHOD_INFO_EX</a> structures in <b>pEapMethods</b>.


### -field pEapMethods

Pointer to the address of the first element in an array of <a href="https://msdn.microsoft.com/2d25f418-2130-4f9c-b3f4-f639dfba020a">EAP_METHOD_INFO_EX</a> structures. The total number of elements is specified in <b>dwNumberOfMethods</b>.


## -see-also




<a href="https://msdn.microsoft.com/f6f3b909-1e89-47f8-853c-c0f3f2414817">Common EAPHost API Structures</a>



<a href="https://msdn.microsoft.com/10407b85-5d2c-4c75-9b65-a0d65d4cc7ab">EAP Method Properties</a>



<a href="https://msdn.microsoft.com/89b5dcbd-afa9-40a8-ab04-2caee01ce0a3">EAP_METHOD_INFO</a>



<a href="https://msdn.microsoft.com/a3e2d5c0-eacd-46de-b092-6fd749870881">EAP_METHOD_INFO_ARRAY</a>



<a href="https://msdn.microsoft.com/2d25f418-2130-4f9c-b3f4-f639dfba020a">EAP_METHOD_INFO_EX</a>



<a href="https://msdn.microsoft.com/47702dd9-d9c2-4dd5-a12d-23a55b031d27">EAP_METHOD_TYPE</a>
 

 

