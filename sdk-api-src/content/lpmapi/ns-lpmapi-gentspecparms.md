---
UID: NS:lpmapi.__unnamed_struct_18
title: GenTspecParms
author: windows-sdk-content
description: The GenTspecParms structure stores generic Tspec parameters.
old-location: qos\gentspecparms.htm
tech.root: QOS
ms.assetid: 8a702e7c-0dfd-48f5-8612-d64d19f2a55c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GenTspecParms, GenTspecParms structure [QOS], lpmapi/GenTspecParms, qos.gentspecparms
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
 - GenTspecParms
product: Windows
targetos: Windows
req.typenames: GenTspecParms
req.redist: 
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




<a href="https://msdn.microsoft.com/en-us/library/Aa373707(v=VS.85).aspx">GenTspec</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa373725(v=VS.85).aspx">IntServTspecBody</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374106(v=VS.85).aspx">QualAppFlowSpec</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374112(v=VS.85).aspx">QualTspec</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374114(v=VS.85).aspx">QualTspecParms</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374418(v=VS.85).aspx">SENDER_TSPEC</a>
 

 

