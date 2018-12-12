---
UID: NS:lpmapi.__unnamed_struct_22
title: QualAppFlowSpec
author: windows-sdk-content
description: The QualAppFlowSpec structure contains FLOWSPEC information for a qualitative application.
old-location: qos\qualappflowspec.htm
tech.root: QOS
ms.assetid: 4e15b094-4250-4699-b66e-6734cf37cbb6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: QualAppFlowSpec, QualAppFlowSpec structure [QOS], lpmapi/QualAppFlowSpec, qos.qualappflowspec
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
 - QualAppFlowSpec
product: Windows
targetos: Windows
req.typenames: QualAppFlowSpec
req.redist: 
---

# QualAppFlowSpec structure


## -description


The 
<b>QualAppFlowSpec</b> structure contains FLOWSPEC information for a qualitative application.


## -struct-fields




### -field Q_spec_serv_hdr

General information and length information for the QualAppFlowSpec object (this structure), expressed as an <a href="https://msdn.microsoft.com/en-us/library/Aa373724(v=VS.85).aspx">IntServServiceHdr</a> structure.


### -field Q_spec_parm_hdr

Parameter header, expressed as an <a href="https://msdn.microsoft.com/en-us/library/Aa373723(v=VS.85).aspx">IntServParmHdr</a> structure.


### -field Q_spec_parms

QUALITATIVE Tspec parameters, expressed as a <a href="https://msdn.microsoft.com/en-us/library/Aa374114(v=VS.85).aspx">QualTspecParms</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa373723(v=VS.85).aspx">IntServParmHdr</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa373724(v=VS.85).aspx">IntServServiceHdr</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374114(v=VS.85).aspx">QualTspecParms</a>
 

 

