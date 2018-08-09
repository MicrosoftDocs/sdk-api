---
UID: NS:lpmapi.GenTspecParms
title: GenTspecParms
author: windows-sdk-content
description: The GenTspecParms structure stores generic Tspec parameters.
old-location: qos\gentspecparms.htm
old-project: qos
ms.assetid: 8a702e7c-0dfd-48f5-8612-d64d19f2a55c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GenTspecParms, GenTspecParms structure [QOS], lpmapi/GenTspecParms, qos.gentspecparms
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
tech.root: 
req.typenames: GenTspecParms
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lpmapi.h
api_name:
 - GenTspecParms
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# GenTspecParms structure


## -description


The 
<b>GenTspecParms</b> structure stores generic Tspec parameters.


## -struct-fields




### -field TB_Tspec_r

Token bucket rate, in bytes per second.


### -field TB_Tspec_b

Token bucket depth, in bytes.


### -field TB_Tspec_p

Peak data rate, in bytes per second.


### -field TB_Tspec_m

Minimum policed unit, in bytes.


### -field TB_Tspec_M

Maximum packet size, in bytes.


## -see-also




<a href="https://msdn.microsoft.com/cefd94ed-ed54-471d-97fc-d523cedd71d6">GenTspec</a>



<a href="https://msdn.microsoft.com/c4244dba-237a-437b-94b7-fd814edb3506">IntServTspecBody</a>



<a href="https://msdn.microsoft.com/4e15b094-4250-4699-b66e-6734cf37cbb6">QualAppFlowSpec</a>



<a href="https://msdn.microsoft.com/dc22de18-3e9f-4b92-aba4-579aa47fab64">QualTspec</a>



<a href="https://msdn.microsoft.com/f9afa6f9-1de7-469e-a317-2dea98c8291c">QualTspecParms</a>



<a href="https://msdn.microsoft.com/d7905687-1af8-4469-b8de-a2445afa90f4">SENDER_TSPEC</a>
 

 

