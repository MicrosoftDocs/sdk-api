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

# _SL_GENUINE_STATE enumeration


## -description


Specifies the state of an application installation.


## -enum-fields




### -field SL_GEN_STATE_IS_GENUINE

The installation is genuine.


### -field SL_GEN_STATE_INVALID_LICENSE

The application does not have a valid license.


### -field SL_GEN_STATE_TAMPERED

The <b>Tampered</b> flag of the license associated with the application is set.


### -field SL_GEN_STATE_OFFLINE

The <b>Offline</b> flag of the license associated with the application is set.


### -field SL_GEN_STATE_LAST

The state of the installation has not changed since the last time it was checked.

