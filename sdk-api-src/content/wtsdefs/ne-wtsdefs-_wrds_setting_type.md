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

# _WRDS_SETTING_TYPE enumeration


## -description


Specifies the category of settings being stored in a <a href="https://msdn.microsoft.com/38AD33F9-F955-4906-90E2-3FE5261A3E58">WRDS_SETTINGS</a> structure.


## -enum-fields




### -field WRDS_SETTING_TYPE_INVALID

The setting type is not defined.


### -field WRDS_SETTING_TYPE_MACHINE

The settings apply to group policy for the computer.


### -field WRDS_SETTING_TYPE_USER

The settings apply to group policy for the user.


### -field WRDS_SETTING_TYPE_SAM

The settings apply to the user security accounts manager (SAM).

