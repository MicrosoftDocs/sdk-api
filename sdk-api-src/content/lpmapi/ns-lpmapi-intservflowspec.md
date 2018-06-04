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

# IntServFlowSpec structure


## -description


The 
<b>IntServFlowSpec</b> structure contains information about Integrated Services flowspecs.


## -struct-fields




### -field spec_mh

General information and length information for the  flowspec object (this structure), expressed as an <a href="https://msdn.microsoft.com/b67fdf53-322b-4a70-ae83-63d4365e9b57">IntServMainHdr</a> structure.


### -field spec_u

Union containing flowspec information.


### -field spec_u.CL_spec

Controlled load flowspec information, expressed as a <a href="https://msdn.microsoft.com/def835ae-f0d2-4cdc-a498-315c4ef1245b">CtrlLoadFlowspec</a> structure.


### -field spec_u.G_spec

Guaranteed service flowspec information, expressed as a <a href="https://msdn.microsoft.com/549380cc-b4ac-414a-9058-f506741f1e76">GuarFlowSpec</a> structure.


### -field spec_u.Q_spec

Qualitative application flowspec information, expressed as a <a href="https://msdn.microsoft.com/4e15b094-4250-4699-b66e-6734cf37cbb6">QualAppFlowSpec</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/def835ae-f0d2-4cdc-a498-315c4ef1245b">CtrlLoadFlowspec</a>



<a href="https://msdn.microsoft.com/549380cc-b4ac-414a-9058-f506741f1e76">GuarFlowSpec</a>



<a href="https://msdn.microsoft.com/4e15b094-4250-4699-b66e-6734cf37cbb6">QualAppFlowSpec</a>
 

 

