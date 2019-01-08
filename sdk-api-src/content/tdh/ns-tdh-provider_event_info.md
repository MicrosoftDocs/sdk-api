---
UID: NS:tdh._PROVIDER_EVENT_INFO
title: PROVIDER_EVENT_INFO
author: windows-sdk-content
description: Defines an array of events in a provider manifest.
old-location: etw\provider_event_info.htm
tech.root: ETW
ms.assetid: CC392841-7436-4543-A846-FB5A27D9A014
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PPROVIDER_EVENT_INFO, PPROVIDER_EVENT_INFO, PPROVIDER_EVENT_INFO structure pointer [ETW], PROVIDER_EVENT_INFO, PROVIDER_EVENT_INFO structure [ETW], etw.provider_event_info, tdh/PPROVIDER_EVENT_INFO, tdh/PROVIDER_EVENT_INFO"
ms.topic: struct
req.header: tdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tdh.h
api_name:
 - PROVIDER_EVENT_INFO
product: Windows
targetos: Windows
req.typenames: PROVIDER_EVENT_INFO
req.redist: 
---

# PROVIDER_EVENT_INFO structure


## -description


The <b>PROVIDER_EVENT_INFO</b> structure defines an array of events in a provider manifest.


## -struct-fields




### -field NumberOfEvents

The number of elements in the <b>EventDescriptorsArray</b> array.


### -field Reserved

Reserved.


### -field EventDescriptorsArray

An array of <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a> structures that contain information about each event.


## -see-also




<a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/93A03E1D-4047-49F1-987B-FB7BE03E0483">TdhEnumerateManifestProviderEvents</a>



<a href="https://msdn.microsoft.com/71702F1F-1708-4CA2-9BFB-3D7332AB6129">TdhGetManifestEventInformation</a>
 

 

