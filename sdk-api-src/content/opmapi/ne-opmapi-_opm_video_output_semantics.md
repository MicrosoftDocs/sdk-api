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

# _OPM_VIDEO_OUTPUT_SEMANTICS enumeration


## -description


Specifies whether the <a href="https://msdn.microsoft.com/8bf43577-3535-4f62-ac81-bb7e3c329403">IOPMVideoOutput</a> interface will use Output Protection Manager (OPM) semantics or Certified Output Protection Protocol (COPP) semantics.


## -enum-fields




### -field OPM_VOS_COPP_SEMANTICS

The interface will use COPP semantics.


### -field OPM_VOS_OPM_SEMANTICS

The interface will use OPM semantics.


### -field OPM_VOS_OPM_INDIRECT_DISPLAY




## -see-also




<a href="https://msdn.microsoft.com/e72e0a5e-476d-41f0-9139-54c4c488053f">OPM Enumerations</a>



<a href="https://msdn.microsoft.com/c034ac81-43d4-482a-9dad-234d33a15046">OPMGetVideoOutputsFromHMONITOR</a>



<a href="https://msdn.microsoft.com/9b287058-9e06-4c40-84f4-506aefce5b8a">OPMGetVideoOutputsFromIDirect3DDevice9Object</a>
 

 

