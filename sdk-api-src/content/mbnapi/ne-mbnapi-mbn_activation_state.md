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

# MBN_ACTIVATION_STATE enumeration


## -description


The <b>MBN_ACTIVATION_STATE</b> enumerated type indicates the current data connection state.


## -enum-fields




### -field MBN_ACTIVATION_STATE_NONE

The connection state is unknown.


### -field MBN_ACTIVATION_STATE_ACTIVATED

The connection has been established.


### -field MBN_ACTIVATION_STATE_ACTIVATING

The device is establishing the connection.


### -field MBN_ACTIVATION_STATE_DEACTIVATED

There is no connection.


### -field MBN_ACTIVATION_STATE_DEACTIVATING

The device is in the process of disconnection.

