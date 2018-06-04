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

# _IMAPI_FORMAT2_RAW_CD_WRITE_ACTION enumeration


## -description


Defines values that indicate the current state of the write operation when using the <a href="https://msdn.microsoft.com/b1988883-459c-46f1-a0d1-df9500a000e1">IDiscFormat2RawCDEventArgs</a> interface.


## -enum-fields




### -field IMAPI_FORMAT2_RAW_CD_WRITE_ACTION_UNKNOWN

Indicates an unknown state.


### -field IMAPI_FORMAT2_RAW_CD_WRITE_ACTION_PREPARING

Preparing to write the session.


### -field IMAPI_FORMAT2_RAW_CD_WRITE_ACTION_WRITING

Writing session data.


### -field IMAPI_FORMAT2_RAW_CD_WRITE_ACTION_FINISHING

Synchronizing the drive's cache with the end of the data written to disc.


## -see-also




<a href="https://msdn.microsoft.com/abe35eee-63a4-4109-8927-825f86b6e302">DDiscFormat2RawCDEvents::Update</a>
 

 

