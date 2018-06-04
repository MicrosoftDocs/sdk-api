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

# _ADRENTRY structure


## -description


Do not use. Describes zero or more properties belonging to one or more recipients.


## -struct-fields




### -field ulReserved1

Type: <b>ULONG</b>


### -field cValues

Type: <b>ULONG</b>

Variable of type <b>ULONG</b> that specifies the count of properties in the property value array to which the <b>rgPropVals</b> member points. The <b>cValues</b> member can be zero.


### -field rgPropVals

Type: <b>LPSPropValue</b>

Pointer to a variable of type <a href="https://msdn.microsoft.com/cff1b41d-fc53-4987-8823-04cbd51e811b">SPropValue</a> that specifies the property value array describing the properties for the recipient. The <b>rgPropVals</b> member can be <b>NULL</b>.

