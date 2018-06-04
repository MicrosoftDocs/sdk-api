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

# _DECODING_SOURCE enumeration


## -description



		Defines the source of the event data.


## -enum-fields




### -field DecodingSourceXMLFile

The source of the event data is a XML manifest.


### -field DecodingSourceWbem

The source of the event data is a WMI MOF class.


### -field DecodingSourceWPP

The source of the event data is a TMF file.


### -field DecodingSourceTlg

Indicates that the event was a self-describing event and was decoded using TraceLogging metadata.


### -field DecodingSourceMax




## -see-also




<a href="https://msdn.microsoft.com/ecf57a23-0dd2-4954-82ac-e92f651c226f">TRACE_EVENT_INFO</a>
 

 

