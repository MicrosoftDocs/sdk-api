---
UID: NS:lpmapi.GuarFlowSpec
title: GuarFlowSpec
author: windows-sdk-content
description: The GuarFlowSpec structure contains guaranteed flowspec information.
old-location: qos\guarflowspec.htm
tech.root: QOS
ms.assetid: 549380cc-b4ac-414a-9058-f506741f1e76
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GuarFlowSpec, GuarFlowSpec structure [QOS], lpmapi/GuarFlowSpec, qos.guarflowspec
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - GuarFlowSpec
product: Windows
targetos: Windows
req.typenames: GuarFlowSpec
req.redist: 
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
 

 

