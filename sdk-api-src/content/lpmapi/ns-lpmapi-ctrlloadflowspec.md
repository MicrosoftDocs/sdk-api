---
UID: NS:lpmapi.CtrlLoadFlowspec
title: CtrlLoadFlowspec
author: windows-sdk-content
description: The CtrlLoadFlowspec structure contains a Controlled Load FLOWSPEC.
old-location: qos\ctrlloadflowspec.htm
tech.root: QOS
ms.assetid: def835ae-f0d2-4cdc-a498-315c4ef1245b
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CtrlLoadFlowspec, CtrlLoadFlowspec structure [QOS], lpmapi/CtrlLoadFlowspec, qos.ctrlloadflowspec
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
 - CtrlLoadFlowspec
product: Windows
targetos: Windows
req.typenames: CtrlLoadFlowspec
req.redist: 
---

# CtrlLoadFlowspec structure


## -description


The 
<b>CtrlLoadFlowspec</b> structure contains a Controlled Load FLOWSPEC.


## -struct-fields




### -field CL_spec_serv_hdr

General information and length information for the controlled load flowspec object (this structure), expressed as an <a href="https://msdn.microsoft.com/63e6a944-f16e-4b90-ab77-22e5c8ef3fb2">IntServServiceHdr</a> structure.


### -field CL_spec_parm_hdr

Parameter header, expressed as an <a href="https://msdn.microsoft.com/56ca242e-d5e9-4c16-9c8e-70a356375683">IntServParmHdr</a> structure.


### -field CL_spec_parms

Generic Tspec  parameters, expressed as a <a href="https://msdn.microsoft.com/8a702e7c-0dfd-48f5-8612-d64d19f2a55c">GenTspecParms</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/8a702e7c-0dfd-48f5-8612-d64d19f2a55c">GenTspecParms</a>



<a href="https://msdn.microsoft.com/56ca242e-d5e9-4c16-9c8e-70a356375683">IntServParmHdr</a>



<a href="https://msdn.microsoft.com/63e6a944-f16e-4b90-ab77-22e5c8ef3fb2">IntServServiceHdr</a>
 

 

