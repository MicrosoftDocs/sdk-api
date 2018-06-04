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

# EcOpenSubscription function


## -description


The <b>EcOpenSubscription</b> function is used to open an existing subscription or create a new subscription according to the flag value specified.


## -parameters




### -param SubscriptionName [in]

Specifies the name of the subscription. The value provided for this parameter should be unique within the computer's scope.


### -param AccessMask [in]

An access mask that specifies the desired access rights to the subscription. Use the <a href="https://msdn.microsoft.com/2ba862f9-6849-43b3-8914-e18ede1d63c0">EC_READ_ACCESS</a> or <a href="https://msdn.microsoft.com/2ba862f9-6849-43b3-8914-e18ede1d63c0">EC_WRITE_ACCESS</a> constants to specify the access rights. The function fails if the security descriptor of the subscription does not permit the requested access for the calling process.


### -param Flags [in]

A value specifying whether a new or existing subscription will be opened. Use the <b>EC_CREATE_NEW</b>, <b>EC_OPEN_ALWAYS</b>, or <b>EC_OPEN_EXISTING</b> constants.


## -returns



If the function succeeds, it returns an handle (<a href="https://msdn.microsoft.com/b78bdaf8-e034-40fe-acf8-632313e4fd94">EC_HANDLE</a>) to a new subscription object. Returns <b>NULL</b> otherwise, in which case use the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function to obtain the error code.




## -see-also




<a href="https://msdn.microsoft.com/48155df6-ba9c-4abe-ba84-6190cee95878">Windows Event Collector Functions</a>
 

 

