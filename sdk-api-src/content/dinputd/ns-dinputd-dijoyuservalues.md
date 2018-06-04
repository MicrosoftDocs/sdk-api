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

# DIJOYUSERVALUES structure


## -description


The <b>DIJOYUSERVALUES</b> structure contains information about the user's joystick settings. 


## -struct-fields




### -field dwSize

Specifies the size of the structure in bytes. This member must be initialized before the structure is used. 


### -field ruv

Joystick user configuration. In addition to the fields contained in the mmddk.h header file, the previously unused <b>jrvRanges.jpCenter</b> field contains the user saturation levels for each axis. A control panel application sets the dead zone and saturation values based on the values set by the end-user during calibration or fine-tuning. Dead zone can be interpreted as "sensitivity in the center" and saturation can be interpreted as "sensitivity along the edges". 


### -field wszGlobalDriver

The global port driver. 


### -field wszGameportEmulator

Unused. 

