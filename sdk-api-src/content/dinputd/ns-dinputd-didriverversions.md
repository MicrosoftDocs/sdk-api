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

# DIDRIVERVERSIONS structure


## -description


The <b>DIDRIVERVERSIONS</b> structure is used by the DirectInput effect driver to report version information back to DirectInput. The semantics of the version numbers are left to the discretion of the device driver. The only requirement is that later versions have higher version numbers than earlier versions. 


## -struct-fields




### -field dwSize

Specifies the size of the structure in bytes. This member must be initialized before the structure is used. 


### -field dwFirmwareRevision

Specifies the firmware revision of the device. 


### -field dwHardwareRevision

Specifies the hardware revision of the device. 


### -field dwFFDriverVersion

Specifies the version number of the force-feedback device driver. 

