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

General information and length information for the  flowspec object (this structure), expressed as an <a href="https://msdn.microsoft.com/en-us/library/Aa373722(v=VS.85).aspx">IntServMainHdr</a> structure.


### -field spec_u

Union containing flowspec information.



#### CL_spec

Controlled load flowspec information, expressed as a <a href="https://msdn.microsoft.com/en-us/library/Aa373430(v=VS.85).aspx">CtrlLoadFlowspec</a> structure.



#### G_spec

Guaranteed service flowspec information, expressed as a <a href="https://msdn.microsoft.com/en-us/library/Aa373710(v=VS.85).aspx">GuarFlowSpec</a> structure.



#### Q_spec

Qualitative application flowspec information, expressed as a <a href="https://msdn.microsoft.com/en-us/library/Aa374106(v=VS.85).aspx">QualAppFlowSpec</a> structure.


### -field CL_spec

 


### -field G_spec

 


### -field Q_spec

 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa373430(v=VS.85).aspx">CtrlLoadFlowspec</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa373710(v=VS.85).aspx">GuarFlowSpec</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374106(v=VS.85).aspx">QualAppFlowSpec</a>
 

 

