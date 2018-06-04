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

# tagCADWORD structure


## -description


Specifies a counted array of values that can be used to obtain the value corresponding to one of the predefined strings for a property.


## -struct-fields




### -field cElems

The size of the array pointed to by <b>pElems</b>.


### -field pElems

A pointer to an array of values, each of which can be passed to the <a href="https://msdn.microsoft.com/a532ebed-3ed8-4b49-a17f-f542fdbd74ff">IPerPropertyBrowsing::GetPredefinedValue</a> method to obtain the corresponding value for one of the property's predefined strings. This array is allocated by the callee using <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a> and is freed by the caller using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


## -see-also




<a href="https://msdn.microsoft.com/730d5e23-e84a-4629-9b59-492d8536122e">CALPOLESTR</a>



<a href="https://msdn.microsoft.com/1b20585f-2bcd-475e-abee-80158692ae0f">IPerPropertyBrowsing::GetPredefinedStrings</a>



<a href="https://msdn.microsoft.com/a532ebed-3ed8-4b49-a17f-f542fdbd74ff">IPerPropertyBrowsing::GetPredefinedValue</a>
 

 

