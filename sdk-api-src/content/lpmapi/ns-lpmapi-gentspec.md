---
UID: NS:lpmapi.GenTspec
title: GenTspec
author: windows-sdk-content
description: The GenTspec structure stores generic Tspec information.
old-location: qos\gentspec.htm
tech.root: QOS
ms.assetid: cefd94ed-ed54-471d-97fc-d523cedd71d6
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GenTspec, GenTspec structure [QOS], lpmapi/GenTspec, qos.gentspec
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: lpmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lpmapi.h
api_name:
 - GenTspec
product: Windows
targetos: Windows
req.typenames: GenTspec
req.redist: 
---

# GenTspec structure


## -description


The 
<b>GenTspec</b> structure stores generic Tspec information.


## -struct-fields




### -field gen_Tspec_serv_hdr

General information and length information for the GenTspec object (this structure), expressed as an <a href="https://msdn.microsoft.com/63e6a944-f16e-4b90-ab77-22e5c8ef3fb2">IntServServiceHdr</a> structure.


### -field gen_Tspec_parm_hdr

Parameter header, expressed as an <a href="https://msdn.microsoft.com/56ca242e-d5e9-4c16-9c8e-70a356375683">IntServParmHdr</a> structure.


### -field gen_Tspec_parms

Tspec parameters, expressed as a <a href="https://msdn.microsoft.com/8a702e7c-0dfd-48f5-8612-d64d19f2a55c">GenTspecParms</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/8a702e7c-0dfd-48f5-8612-d64d19f2a55c">GenTspecParms</a>



<a href="https://msdn.microsoft.com/56ca242e-d5e9-4c16-9c8e-70a356375683">IntServParmHdr</a>



<a href="https://msdn.microsoft.com/63e6a944-f16e-4b90-ab77-22e5c8ef3fb2">IntServServiceHdr</a>



<a href="https://msdn.microsoft.com/c4244dba-237a-437b-94b7-fd814edb3506">IntServTspecBody</a>



<a href="https://msdn.microsoft.com/4e15b094-4250-4699-b66e-6734cf37cbb6">QualAppFlowSpec</a>



<a href="https://msdn.microsoft.com/dc22de18-3e9f-4b92-aba4-579aa47fab64">QualTspec</a>



<a href="https://msdn.microsoft.com/f9afa6f9-1de7-469e-a317-2dea98c8291c">QualTspecParms</a>



<a href="https://msdn.microsoft.com/d7905687-1af8-4469-b8de-a2445afa90f4">SENDER_TSPEC</a>
 

 

