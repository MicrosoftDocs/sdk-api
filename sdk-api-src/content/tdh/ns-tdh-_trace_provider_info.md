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

# _TRACE_PROVIDER_INFO structure


## -description



		Defines the GUID and name for a provider.


## -struct-fields




### -field ProviderGuid

GUID that uniquely identifies the provider.


### -field SchemaSource

Is zero if the provider uses a XML manifest to provide a description of its events. Otherwise, the value is 1 if the provider uses a WMI MOF class to provide a description of its events.


### -field ProviderNameOffset

Offset to a null-terminated Unicode string that contains the name of the provider. The offset is from the beginning of the <a href="https://msdn.microsoft.com/bb4548fb-70e5-4726-bc92-adb7ba7be0e4">PROVIDER_ENUMERATION_INFO</a> buffer that <a href="https://msdn.microsoft.com/ef326ef8-227d-46b5-88b9-b519748fb778">TdhEnumerateProviders</a> returns.


## -see-also




<a href="https://msdn.microsoft.com/bb4548fb-70e5-4726-bc92-adb7ba7be0e4">PROVIDER_ENUMERATION_INFO</a>
 

 

