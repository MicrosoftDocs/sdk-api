---
UID: NS:lpmapi.__unnamed_struct_23
title: IntServTspecBody
author: windows-sdk-content
description: The IntServTspecBody structure contains information for an RSVP Tspec.
old-location: qos\intservtspecbody.htm
tech.root: QOS
ms.assetid: c4244dba-237a-437b-94b7-fd814edb3506
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IntServTspecBody, IntServTspecBody structure [QOS], lpmapi/IntServTspecBody, qos.intservtspecbody
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
 - IntServTspecBody
product: Windows
targetos: Windows
req.typenames: IntServTspecBody
req.redist: 
---

# IntServTspecBody structure


## -description


The 
<b>IntServTspecBody</b> structure contains information for an RSVP Tspec.


## -struct-fields




### -field st_mh

Header for the corresponding Tspec object, expressed as  <a href="https://msdn.microsoft.com/en-us/library/Aa373722(v=VS.85).aspx">IntServMainHdr</a> structure.


### -field tspec_u



#### gen_stspec

Generic Tspec, expressed as a <a href="https://msdn.microsoft.com/en-us/library/Aa373707(v=VS.85).aspx">GenTspec</a> structure.



#### qual_stspec

Qualitative Tspec, expressed as a <a href="https://msdn.microsoft.com/en-us/library/Aa374112(v=VS.85).aspx">QualTspec</a> structure.


### -field gen_stspec

 


### -field qual_stspec

 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa373707(v=VS.85).aspx">GenTspec</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa373722(v=VS.85).aspx">IntServMainHdr</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374112(v=VS.85).aspx">QualTspec</a>
 

 

