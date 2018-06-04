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

# ADDRESS_STATE enumeration


## -description


The 
<b>ADDRESS_STATE</b> enum is used by the 
<a href="https://msdn.microsoft.com/f68d0fb0-126d-4464-9d5a-0ffae4d40cb7">ITAddress::get_State</a> method to check the address state.


## -enum-fields




### -field AS_INSERVICE

Normal state; the address can be used.


### -field AS_OUTOFSERVICE

The address is temporarily out of service, but may go back into service at some time.


## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address object</a>



<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a>



<a href="https://msdn.microsoft.com/f68d0fb0-126d-4464-9d5a-0ffae4d40cb7">ITAddress::get_State</a>
 

 

