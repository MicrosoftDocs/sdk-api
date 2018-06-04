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

# tdTBS_CONTEXT_PARAMS2 structure


## -description


Specifies the version of the TBS context implementation. You must use this structure if your application works with both versions of TPM.

Applications interacting with just TPM 2.0 should pass a pointer to a <b>TBS_CONTEXT_PARAMS2</b> structure, with  <b>version</b> set to TPM_VERSION_20, and <b>includeTpm20</b> set to 1. 

Applications interacting with both TPM 1.2 and TPM 2.0 should pass a pointer to a <b>TBS_CONTEXT_PARAMS2</b> structure, with  <b>version</b> set to TPM_VERSION_20, <b>includeTpm20</b> set to 1, and <b>includeTpm12</b> set to 1. 


## -struct-fields




### -field version

The version of the TBS context implementation. This must be set to 	TPM_VERSION_20.


### -field requestRaw

 


### -field includeTpm12

 


### -field includeTpm20

 


### -field asUINT32

Used to access all of the  bits in one variable.


#### - includeTpm12:1

Set to 1 if the TBS commands are to work on TPM 1.2.


#### - includeTpm20:1

Set to 1 if the TBS commands are to work on TPM 2.0.


#### - requestRaw:1

Set to 1 to request raw content.

