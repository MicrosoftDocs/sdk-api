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

# WSC_SECURITY_PRODUCT_STATE enumeration


## -description


Defines the current state of the security product that is made available to Windows Security Center. 


## -enum-fields




### -field WSC_SECURITY_PRODUCT_STATE_ON

The security product software is turned on and protecting the user.


### -field WSC_SECURITY_PRODUCT_STATE_OFF

The security product software is turned off and protection is disabled.


### -field WSC_SECURITY_PRODUCT_STATE_SNOOZED

The security product software is in the snoozed state, temporarily off,  and not actively protecting the computer.


### -field WSC_SECURITY_PRODUCT_STATE_EXPIRED

The security product software has expired and is no longer actively protecting the computer.

