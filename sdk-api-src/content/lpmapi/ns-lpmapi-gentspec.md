---
UID: NS:lpmapi.__unnamed_struct_19
title: GenTspec
author: windows-sdk-content
description: The GenTspec structure stores generic Tspec information.
old-location: qos\gentspec.htm
tech.root: QOS
ms.assetid: cefd94ed-ed54-471d-97fc-d523cedd71d6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GenTspec, GenTspec structure [QOS], lpmapi/GenTspec, qos.gentspec
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

General information and length information for the GenTspec object (this structure), expressed as an <a href="https://msdn.microsoft.com/en-us/library/Aa373724(v=VS.85).aspx">IntServServiceHdr</a> structure.


### -field gen_Tspec_parm_hdr

Parameter header, expressed as an <a href="https://msdn.microsoft.com/en-us/library/Aa373723(v=VS.85).aspx">IntServParmHdr</a> structure.


### -field gen_Tspec_parms

Tspec parameters, expressed as a <a href="https://msdn.microsoft.com/en-us/library/Aa373708(v=VS.85).aspx">GenTspecParms</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa373708(v=VS.85).aspx">GenTspecParms</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa373723(v=VS.85).aspx">IntServParmHdr</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa373724(v=VS.85).aspx">IntServServiceHdr</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa373725(v=VS.85).aspx">IntServTspecBody</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374106(v=VS.85).aspx">QualAppFlowSpec</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374112(v=VS.85).aspx">QualTspec</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374114(v=VS.85).aspx">QualTspecParms</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374418(v=VS.85).aspx">SENDER_TSPEC</a>
 

 

