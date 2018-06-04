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

# WICRawToneCurve structure


## -description


Represents a raw image tone curve.


## -struct-fields




### -field cPoints

Type: <b>UINT</b>

The number of tone curve points.


### -field aPoints

Type: <b><a href="https://msdn.microsoft.com/c5fbcd25-2884-4313-93d5-c1f290de4a77">WICRawToneCurvePoint</a>[1]</b>

The array of tone curve points.

