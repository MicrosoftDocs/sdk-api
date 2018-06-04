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

# _SecPkgContext_Bindings structure


## -description


Specifies a structure that contains channel binding information for a security <a href="https://msdn.microsoft.com/library/windows/hardware/hh439393">context</a>.


## -struct-fields




### -field BindingsLength

The size, in bytes, of the structure specified by the <b>Bindings</b> member


### -field Bindings

A pointer to a <a href="https://msdn.microsoft.com/1cdbe53f-3fa0-46b1-9449-8fd3db6cddce">SEC_CHANNEL_BINDINGS</a> structure that specifies channel binding information.


## -see-also




<a href="https://msdn.microsoft.com/0329e525-a743-4e6c-aac4-9f74274dadd2">QueryContextAttributes (Schannel)</a>
 

 

