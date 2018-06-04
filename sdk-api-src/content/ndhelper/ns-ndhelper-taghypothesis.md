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

# tagHYPOTHESIS structure


## -description


The <b>HYPOTHESIS</b> structure contains data used to submit a hypothesis to NDF for another  helper class. The name of the helper class, the number of parameters that the helper class requires, and the parameters to pass to the helper class are contained in this structure.


## -struct-fields




### -field pwszClassName

Type: <b>[string] LPWSTR</b>

A pointer to a null-terminated string that contains the name of the helper class.


### -field pwszDescription

Type: <b>[string] LPWSTR</b>

A  pointer to a null-terminated string that contains a user-friendly description of the data being passed to the helper class..


### -field celt

Type: <b>ULONG</b>

The count of attributes in this hypothesis.


### -field rgAttributes

Type: <b>[size_is(celt)]PHELPER_ATTRIBUTE[ ]</b>

A pointer to an array of <a href="https://msdn.microsoft.com/bff9303e-7fab-49af-b213-aa0a9c83676e">HELPER_ATTRIBUTE</a> structures that contains key attributes for this hypothesis. 


## -see-also




<a href="https://msdn.microsoft.com/bff9303e-7fab-49af-b213-aa0a9c83676e">HELPER_ATTRIBUTE</a>
 

 

