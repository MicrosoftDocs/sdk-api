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

# PHONE_PRIVILEGE enumeration


## -description


The 
<b>PHONE_PRIVILEGE</b> enum indicates the application's privilege status with respect to the current phone device.


## -enum-fields




### -field PP_OWNER

The application has owner privileges for the current phone session.


### -field PP_MONITOR

The application has monitor privileges for the current phone session.


## -see-also




<a href="https://msdn.microsoft.com/d9efe2f7-3628-4e1f-b554-a6889d82a973">ITPhone::Open</a>



<a href="https://msdn.microsoft.com/88103a48-a5cd-43a7-a88e-9b16313b35c2">ITPhone::get_Privilege</a>
 

 

