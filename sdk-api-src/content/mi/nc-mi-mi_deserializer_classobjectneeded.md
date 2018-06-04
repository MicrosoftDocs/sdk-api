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

# MI_Deserializer_ClassObjectNeeded callback function


## -description


Used to provide requested class object during deserialization.


## -parameters




### -param *context [in, optional]

A pointer to the context.


### -param *serverName [in, optional]

The name of the server.


### -param *namespaceName [in, optional]

The namespace of the object.


### -param *className [in, optional]

The class of the object.


#### - **requestedClassObject [out]

A <a href="https://msdn.microsoft.com/7f02e0fa-9e58-455d-9cf4-1d1244c44422">MI_Class</a> representing the requested class object.


#### - requestedClassObject [out]

A <a href="https://msdn.microsoft.com/7f02e0fa-9e58-455d-9cf4-1d1244c44422">MI_Class</a> representing the requested class object.


## -returns



Returns a <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> indicating the status of the operation.




## -see-also




<a href="https://msdn.microsoft.com/dcd2b458-7c25-47a8-a324-43fc1456fcec">MI_DeserializerFT</a>



<a href="https://msdn.microsoft.com/09ad196c-9940-4d10-8a4e-1e06acd5d677">MI_Deserializer_DeserializeClass</a>



<a href="https://msdn.microsoft.com/54b24a50-f700-4369-b6dc-8406000a5b30">MI_Deserializer_DeserializeInstance</a>
 

 

