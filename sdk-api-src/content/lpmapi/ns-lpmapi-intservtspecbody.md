---
UID: NS:lpmapi.IntServTspecBody
title: IntServTspecBody
author: windows-sdk-content
description: The IntServTspecBody structure contains information for an RSVP Tspec.
old-location: qos\intservtspecbody.htm
old-project: qos
ms.assetid: c4244dba-237a-437b-94b7-fd814edb3506
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IntServTspecBody, IntServTspecBody structure [QOS], lpmapi/IntServTspecBody, qos.intservtspecbody
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
req.typenames: IntServTspecBody
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
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IntServTspecBody structure


## -description


The 
<b>IntServTspecBody</b> structure contains information for an RSVP Tspec.


## -struct-fields




### -field st_mh

Header for the corresponding Tspec object, expressed as  <a href="https://msdn.microsoft.com/b67fdf53-322b-4a70-ae83-63d4365e9b57">IntServMainHdr</a> structure.


### -field tspec_u


### -field tspec_u.gen_stspec

Generic Tspec, expressed as a <a href="https://msdn.microsoft.com/cefd94ed-ed54-471d-97fc-d523cedd71d6">GenTspec</a> structure.


### -field tspec_u.qual_stspec

Qualitative Tspec, expressed as a <a href="https://msdn.microsoft.com/dc22de18-3e9f-4b92-aba4-579aa47fab64">QualTspec</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/cefd94ed-ed54-471d-97fc-d523cedd71d6">GenTspec</a>



<a href="https://msdn.microsoft.com/b67fdf53-322b-4a70-ae83-63d4365e9b57">IntServMainHdr</a>



<a href="https://msdn.microsoft.com/dc22de18-3e9f-4b92-aba4-579aa47fab64">QualTspec</a>
 

 

