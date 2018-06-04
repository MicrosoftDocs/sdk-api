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

# FULLDUPLEX_SUPPORT enumeration


## -description


The 
<b>FULLDUPLEX_SUPPORT</b> enum is used by applications interacting with legacy TSPs to indicate whether a specified terminal supports full duplex operations. This enum is returned by the 
<a href="https://msdn.microsoft.com/117586d7-8214-4fc8-9c7d-08865582cc2a">ITLegacyWaveSupport::IsFullDuplex</a> method.


## -enum-fields




### -field FDS_SUPPORTED

Full duplex supported.


### -field FDS_NOTSUPPORTED

Full duplex not supported.


### -field FDS_UNKNOWN

The TSP cannot determine whether the device is full duplex.


## -see-also




<a href="https://msdn.microsoft.com/117586d7-8214-4fc8-9c7d-08865582cc2a">ITLegacyWaveSupport::IsFullDuplex</a>
 

 

