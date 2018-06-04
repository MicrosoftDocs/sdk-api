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

# DIEFFESCAPE structure


## -description


The <b>DIEFFESCAPE</b> structure passes hardware-specific data directly to the device driver. 


## -struct-fields




### -field dwSize

Specifies the size of the structure in bytes. This member must be initialized before the structure is used. 


### -field dwCommand

Specifies a driver-specific command number. Contact the hardware vendor for a list of valid commands and their parameters. 


### -field lpvInBuffer

Points to the buffer containing the data required to perform the operation. 


### -field cbInBuffer

Specifies the size, in bytes, of the <b>lpvInBuffer</b> buffer. 


### -field lpvOutBuffer

Points to the buffer in which the operation's output data is returned. 


### -field cbOutBuffer

On entry, specifies the size, in bytes, of the <b>lpvOutBuffer</b> buffer. On exit, specifies the number of bytes actually produced by the command. 

