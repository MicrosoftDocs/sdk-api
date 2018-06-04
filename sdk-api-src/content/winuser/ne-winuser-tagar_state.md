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

# tagAR_STATE enumeration


## -description


Indicates the state of screen auto-rotation for the system. For example, whether auto-rotation is supported, and whether it is enabled by the user. This enum is a bitwise OR of one or more of the following values.


## -enum-fields




### -field AR_ENABLED

            Auto-rotation is enabled by the user.


### -field AR_DISABLED

Auto-rotation is disabled by the user.


### -field AR_SUPPRESSED

Auto-rotation is currently suppressed by one or more process auto-rotation preferences.


### -field AR_REMOTESESSION

The session is remote, and auto-rotation is temporarily disabled as a result.


### -field AR_MULTIMON

The system has multiple monitors attached, and auto-rotation is temporarily disabled as a result.


### -field AR_NOSENSOR

The system does not have an auto-rotation sensor.


### -field AR_NOT_SUPPORTED

Auto-rotation is not supported with the current system configuration.


### -field AR_DOCKED

The device is docked, and auto-rotation is temporarily disabled as a result.


### -field AR_LAPTOP

The device is in laptop mode, and auto-rotation is temporarily disabled as a result.

