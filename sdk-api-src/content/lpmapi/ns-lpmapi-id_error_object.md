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

# ID_ERROR_OBJECT structure


## -description


The 
<b>ID_ERROR_OBJECT</b> structure contains error message information for Identity Policy Elements for RSVP.


## -struct-fields




### -field usIdErrLength

Length of <b>udIdErrData</b>, in bytes.


### -field ucAType

Type of Identity Policy Element error. 


### -field ucSubType

Sub-type of the Identity Policy Element error.


### -field usReserved

Reserved. Do not use.


### -field usIdErrorValue

Value for the Identity Policy Element error.


### -field ucIdErrData

Identity Policy Element error data.


## -see-also




<a href="https://msdn.microsoft.com/72eeb985-85e2-48c6-b79f-73f48295740a">Policy Elements</a>
 

 

