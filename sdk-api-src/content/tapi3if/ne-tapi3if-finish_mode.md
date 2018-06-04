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

# FINISH_MODE enumeration


## -description


The 
<b>FINISH_MODE</b> enum is used by applications to indicate the type of call finish required. Operations that the TAPI DLL performs vary depending on whether a call transfer is being completed or a call is being added to a conference.


## -enum-fields




### -field FM_ASTRANSFER

A call transfer is being finished.


### -field FM_ASCONFERENCE

A call is being added to a conference call.


## -see-also




<a href="https://msdn.microsoft.com/3b0bd871-b618-4c24-a717-62a248112d97">ITBasicCallControl::Finish</a>
 

 

