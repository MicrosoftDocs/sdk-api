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

# TAPIOBJECT_EVENT enumeration


## -description


The 
<b>TAPIOBJECT_EVENT</b> enum describes TAPI object events. The 
<a href="https://msdn.microsoft.com/5ae4362f-6987-461e-928f-9478e37e0380">ITTAPIObjectEvent::get_Event</a> method returns a member of this enum to indicate the type of TAPI object event that occurred.


## -enum-fields




### -field TE_ADDRESSCREATE

A new address has been created.


### -field TE_ADDRESSREMOVE

An address has been moved.


### -field TE_REINIT

The TAPI object has been reinitialized


### -field TE_TRANSLATECHANGE

A translation change has occurred.


### -field TE_ADDRESSCLOSE

Address has been closed.


### -field TE_PHONECREATE


### -field TE_PHONEREMOVE




## -see-also




<a href="https://msdn.microsoft.com/5ae4362f-6987-461e-928f-9478e37e0380">ITTAPIObjectEvent::get_Event</a>
 

 

