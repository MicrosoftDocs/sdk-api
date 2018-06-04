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

# _HTTP_SERVICE_BINDING_A structure


## -description


The <b>HTTP_SERVICE_BINDING_A</b> structure provides  Service Principle Name (SPN) in ASCII. 


## -struct-fields




### -field Base

An <a href="https://msdn.microsoft.com/c9d3ed21-8987-4b98-99a1-dc1e776b0dab">HTTP_SERVICE_BINDING_BASE</a> value,  the <b>Type</b> member of which must be set to <b>HttpServiceBindingTypeA</b>. 


### -field Buffer

A pointer to a buffer that represents the SPN.


### -field BufferSize

The length, in bytes, of the string in <b>Buffer</b>.

