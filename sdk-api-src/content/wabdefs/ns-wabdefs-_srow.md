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

# _SRow structure


## -description


Do not use. Describes a row from a table containing selected properties for a specific object.


## -struct-fields




### -field ulAdrEntryPad

Type: <b>ULONG</b>

Variable of type <b>ULONG</b> that specifies the number of padding bytes for aligning properly the property values to which the <b>lpProps</b> member points.


### -field cValues

Type: <b>ULONG</b>

Variable of type <b>ULONG</b> that specifies the count of property values to which <b>lpProps</b> points.


### -field lpProps

Type: <b>LPSPropValue</b>

Pointer to an array of variables of type <a href="https://msdn.microsoft.com/cff1b41d-fc53-4987-8823-04cbd51e811b">SPropValue</a> that describe the property values for the columns in the row.

