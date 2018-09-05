---
UID: NS:lpmapi.QualAppFlowSpec
title: QualAppFlowSpec
author: windows-sdk-content
description: The QualAppFlowSpec structure contains FLOWSPEC information for a qualitative application.
old-location: qos\qualappflowspec.htm
old-project: QOS
ms.assetid: 4e15b094-4250-4699-b66e-6734cf37cbb6
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: QualAppFlowSpec, QualAppFlowSpec structure [QOS], lpmapi/QualAppFlowSpec, qos.qualappflowspec
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: lpmapi.h
req.include-header: 
req.redist: 
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
req.typenames: QualAppFlowSpec
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lpmapi.h
api_name:
 - QualAppFlowSpec
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# QualAppFlowSpec structure


## -description


The 
<b>QualAppFlowSpec</b> structure contains FLOWSPEC information for a qualitative application.


## -struct-fields




### -field Q_spec_serv_hdr

General information and length information for the QualAppFlowSpec object (this structure), expressed as an <a href="https://msdn.microsoft.com/63e6a944-f16e-4b90-ab77-22e5c8ef3fb2">IntServServiceHdr</a> structure.


### -field Q_spec_parm_hdr

Parameter header, expressed as an <a href="https://msdn.microsoft.com/56ca242e-d5e9-4c16-9c8e-70a356375683">IntServParmHdr</a> structure.


### -field Q_spec_parms

QUALITATIVE Tspec parameters, expressed as a <a href="https://msdn.microsoft.com/f9afa6f9-1de7-469e-a317-2dea98c8291c">QualTspecParms</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/56ca242e-d5e9-4c16-9c8e-70a356375683">IntServParmHdr</a>



<a href="https://msdn.microsoft.com/63e6a944-f16e-4b90-ab77-22e5c8ef3fb2">IntServServiceHdr</a>



<a href="https://msdn.microsoft.com/f9afa6f9-1de7-469e-a317-2dea98c8291c">QualTspecParms</a>
 

 

