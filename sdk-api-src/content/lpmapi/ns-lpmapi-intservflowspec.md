---
UID: NS:lpmapi.__unnamed_struct_28
title: IntServFlowSpec
author: windows-sdk-content
description: The IntServFlowSpec structure contains information about Integrated Services flowspecs.
old-location: qos\intservflowspec.htm
tech.root: QOS
ms.assetid: c16115ba-03fa-4363-bf16-5341da54f792
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IntServFlowSpec, IntServFlowSpec structure [QOS], lpmapi/IntServFlowSpec, qos.intservflowspec
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
 - IntServFlowSpec
product: Windows
targetos: Windows
req.typenames: IntServFlowSpec
req.redist: 
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



#### CL_spec

Controlled load flowspec information, expressed as a <a href="https://msdn.microsoft.com/def835ae-f0d2-4cdc-a498-315c4ef1245b">CtrlLoadFlowspec</a> structure.



#### G_spec

Guaranteed service flowspec information, expressed as a <a href="https://msdn.microsoft.com/549380cc-b4ac-414a-9058-f506741f1e76">GuarFlowSpec</a> structure.



#### Q_spec

Qualitative application flowspec information, expressed as a <a href="https://msdn.microsoft.com/4e15b094-4250-4699-b66e-6734cf37cbb6">QualAppFlowSpec</a> structure.


### -field CL_spec

 


### -field G_spec

 


### -field Q_spec

 




## -see-also




<a href="https://msdn.microsoft.com/def835ae-f0d2-4cdc-a498-315c4ef1245b">CtrlLoadFlowspec</a>



<a href="https://msdn.microsoft.com/549380cc-b4ac-414a-9058-f506741f1e76">GuarFlowSpec</a>



<a href="https://msdn.microsoft.com/4e15b094-4250-4699-b66e-6734cf37cbb6">QualAppFlowSpec</a>
 

 

