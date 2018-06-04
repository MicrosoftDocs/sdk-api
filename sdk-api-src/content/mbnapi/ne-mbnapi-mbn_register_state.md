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

# MBN_REGISTER_STATE enumeration


## -description


The <b>MBN_REGISTER_STATE</b> enumerated type indicates the network registration state of a Mobile Broadband device.


## -enum-fields




### -field MBN_REGISTER_STATE_NONE

The device registration state is unknown.  This state may be set upon failure of registration mode change requests.


### -field MBN_REGISTER_STATE_DEREGISTERED

The device is not registered and not searching for a provider.


### -field MBN_REGISTER_STATE_SEARCHING

The device is not registered and is searching for a provider.


### -field MBN_REGISTER_STATE_HOME

The device is on a home provider.


### -field MBN_REGISTER_STATE_ROAMING

The device is on a roaming provider.


### -field MBN_REGISTER_STATE_PARTNER

The device is on a roaming partner.


### -field MBN_REGISTER_STATE_DENIED

The device was denied registration.  Emergency voice calls may be made.  This applies to voice and not data.

