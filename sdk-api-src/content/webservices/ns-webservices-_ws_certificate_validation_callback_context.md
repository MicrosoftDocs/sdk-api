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

# _WS_CERTIFICATE_VALIDATION_CALLBACK_CONTEXT structure


## -description


The <b>WS_CERTIFICATE_VALIDATION_CALLBACK_CONTEXT</b> structure contains the callback function and state for validating the certificate for an HTTP connection.


## -struct-fields




### -field callback

A <a href="https://msdn.microsoft.com/368A6162-F194-4C5C-B5FE-89633435168F">WS_CERTIFICATE_VALIDATION_CALLBACK</a> callback that is an application specific callback for validating HTTP certificates.


### -field state

Application specific state that is made available to the callback when invoked.


## -see-also




<a href="https://msdn.microsoft.com/368A6162-F194-4C5C-B5FE-89633435168F">WS_CERTIFICATE_VALIDATION_CALLBACK</a>
 

 

