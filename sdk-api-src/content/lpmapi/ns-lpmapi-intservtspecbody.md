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

# IntServTspecBody structure


## -description


The 
<b>IntServTspecBody</b> structure contains information for an RSVP Tspec.


## -struct-fields




### -field st_mh

Header for the corresponding Tspec object, expressed as  <a href="https://msdn.microsoft.com/b67fdf53-322b-4a70-ae83-63d4365e9b57">IntServMainHdr</a> structure.


### -field tspec_u


### -field tspec_u.gen_stspec

Generic Tspec, expressed as a <a href="https://msdn.microsoft.com/cefd94ed-ed54-471d-97fc-d523cedd71d6">GenTspec</a> structure.


### -field tspec_u.qual_stspec

Qualitative Tspec, expressed as a <a href="https://msdn.microsoft.com/dc22de18-3e9f-4b92-aba4-579aa47fab64">QualTspec</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/cefd94ed-ed54-471d-97fc-d523cedd71d6">GenTspec</a>



<a href="https://msdn.microsoft.com/b67fdf53-322b-4a70-ae83-63d4365e9b57">IntServMainHdr</a>



<a href="https://msdn.microsoft.com/dc22de18-3e9f-4b92-aba4-579aa47fab64">QualTspec</a>
 

 

