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

# _SERVICE_TYPE_INFO_ABSA structure


## -description



			The 
<b>SERVICE_TYPE_INFO_ABS</b> structure contains information about a network service type. Use <b>SERVICE_TYPE_INFO_ABS</b> to add a network service type to a namespace.


## -struct-fields




### -field lpTypeName

Pointer to a zero-terminated string that is the name of the network service type. This name is the same in all namespaces, and is used by the 
<a href="https://msdn.microsoft.com/177bbae5-bc00-4ce5-a0f7-8474f0c2cb2e">GetTypeByName</a> and 
<b>GetNameByType</b> functions.


### -field dwValueCount

Number of 
<a href="https://msdn.microsoft.com/6e3df308-3f5c-40d7-b0f9-19fb6d6d3db8">SERVICE_TYPE_VALUE_ABS</a> structures in the <b>Values</b> member array that follows <b>dwValueCount</b>.


### -field Values

Array of 
<a href="https://msdn.microsoft.com/6e3df308-3f5c-40d7-b0f9-19fb6d6d3db8">SERVICE_TYPE_VALUE_ABS</a> structures. 




Each of these structures contains information about a service type value that the operating system or network service may need when an instance of this network service type is registered with a namespace.

The information in these structures may be specific to a namespace. For example, if a network service uses the SAP namespace, but does not have a <b>GUID</b> that contains the SAP identifier (SAPID), it defines the SAPID in a 
<a href="https://msdn.microsoft.com/6e3df308-3f5c-40d7-b0f9-19fb6d6d3db8">SERVICE_TYPE_VALUE_ABS</a> structure.


## -remarks



When you use the 
<a href="https://msdn.microsoft.com/cc5e35ef-5c64-41ba-a5f9-5961371c4d08">SetService</a> function to add a network service type to a namespace, the 
<b>SERVICE_TYPE_INFO_ABS</b> structure is passed as the <b>ServiceSpecificInfo</b> BLOB member of a 
<a href="https://msdn.microsoft.com/e76e0c1b-8cbf-45ad-a685-fb672801c24d">SERVICE_INFO</a> structure. Although the <b>ServiceSpecificInfo</b> member generally should not contain pointers, an exception is made in the case of the 
<b>SERVICE_TYPE_INFO_ABS</b> and 
<a href="https://msdn.microsoft.com/6e3df308-3f5c-40d7-b0f9-19fb6d6d3db8">SERVICE_TYPE_VALUE_ABS</a> structures.




## -see-also




<a href="https://msdn.microsoft.com/e76e0c1b-8cbf-45ad-a685-fb672801c24d">SERVICE_INFO</a>



<a href="https://msdn.microsoft.com/6e3df308-3f5c-40d7-b0f9-19fb6d6d3db8">SERVICE_TYPE_VALUE_ABS</a>



<a href="https://msdn.microsoft.com/cc5e35ef-5c64-41ba-a5f9-5961371c4d08">SetService</a>
 

 

