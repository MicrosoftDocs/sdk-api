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

# GuarFlowSpec structure


## -description


The 
<b>GuarFlowSpec</b> structure contains guaranteed flowspec information.


## -struct-fields




### -field Guar_serv_hdr

General information and length information for the guaranteed flowspec object (this structure), expressed as an <a href="https://msdn.microsoft.com/63e6a944-f16e-4b90-ab77-22e5c8ef3fb2">IntServServiceHdr</a> structure.


### -field Guar_Tspec_hdr

Parameter header for the guaranteed Tspec, expressed as an <a href="https://msdn.microsoft.com/56ca242e-d5e9-4c16-9c8e-70a356375683">IntServParmHdr</a> structure.


### -field Guar_Tspec_parms

Generic Tspec  parameters, expressed as a <a href="https://msdn.microsoft.com/8a702e7c-0dfd-48f5-8612-d64d19f2a55c">GenTspecParms</a> structure.


### -field Guar_Rspec_hdr

Parameter header for the guaranteed Rspec, expressed as an <a href="https://msdn.microsoft.com/56ca242e-d5e9-4c16-9c8e-70a356375683">IntServParmHdr</a> structure.


### -field Guar_Rspec

Guaranteed rate, in bytes per second, expressed as a <a href="https://msdn.microsoft.com/b5a2daa1-9783-44c2-baa6-5164dedf498f">GuarRspec</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/8a702e7c-0dfd-48f5-8612-d64d19f2a55c">GenTspecParms</a>



<a href="https://msdn.microsoft.com/b5a2daa1-9783-44c2-baa6-5164dedf498f">GuarRspec</a>



<a href="https://msdn.microsoft.com/56ca242e-d5e9-4c16-9c8e-70a356375683">IntServParmHdr</a>



<a href="https://msdn.microsoft.com/63e6a944-f16e-4b90-ab77-22e5c8ef3fb2">IntServServiceHdr</a>
 

 

