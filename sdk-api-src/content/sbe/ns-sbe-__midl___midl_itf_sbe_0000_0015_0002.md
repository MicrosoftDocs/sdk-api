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

# __MIDL___MIDL_itf_sbe_0000_0015_0002 structure


## -description


Describes a stream captured by a tuner.


## -struct-fields




### -field Version

 


### -field StreamId

Specifies a unique identifier for the stream.


### -field Default

Indicates whether or not the stream is the default stream.


### -field Creation

Indicates whether or not the stream has been created.


### -field Reserved

Reserved.


### -field guidSubMediaType

Specifies the GUID corresponding to the media subtype.


### -field guidFormatType

Specifies the GUID corresponding to the major media type of the stream.


### -field MediaType

Defines the major media type of the stream.


#### - version

Specifies the stream's version number.


## -see-also




<a href="https://msdn.microsoft.com/90ac310a-7fd3-440f-9cf7-7d6eb58996cc">Stream Buffer Engine Structures</a>
 

 

