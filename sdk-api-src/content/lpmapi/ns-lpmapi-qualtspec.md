---
UID: NS:lpmapi.__unnamed_struct_21
title: QualTspec
author: windows-sdk-content
description: The QualTspec structure contains qualitative Tspec information.
old-location: qos\qualtspec.htm
tech.root: QOS
ms.assetid: dc22de18-3e9f-4b92-aba4-579aa47fab64
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: QualTspec, QualTspec structure [QOS], lpmapi/QualTspec, qos.qualtspec
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
 - QualTspec
product: Windows
targetos: Windows
req.typenames: QualTspec
req.redist: 
---

# QualTspec structure


## -description


The 
<b>QualTspec</b> structure contains qualitative Tspec information.


## -struct-fields




### -field qual_Tspec_serv_hdr

General information and length information for the QualTspec object (this structure), expressed as an <a href="https://msdn.microsoft.com/63e6a944-f16e-4b90-ab77-22e5c8ef3fb2">IntServServiceHdr</a> structure.


### -field qual_Tspec_parm_hdr

Parameter header, expressed as an <a href="https://msdn.microsoft.com/56ca242e-d5e9-4c16-9c8e-70a356375683">IntServParmHdr</a> structure.


### -field qual_Tspec_parms

Tspec parameters, expressed as a <a href="https://msdn.microsoft.com/f9afa6f9-1de7-469e-a317-2dea98c8291c">QualTspecParms</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/56ca242e-d5e9-4c16-9c8e-70a356375683">IntServParmHdr</a>



<a href="https://msdn.microsoft.com/63e6a944-f16e-4b90-ab77-22e5c8ef3fb2">IntServServiceHdr</a>



<a href="https://msdn.microsoft.com/f9afa6f9-1de7-469e-a317-2dea98c8291c">QualTspecParms</a>
 

 

