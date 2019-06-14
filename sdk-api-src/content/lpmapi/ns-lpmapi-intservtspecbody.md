---
UID: NS:lpmapi.__unnamed_struct_23
title: IntServTspecBody (lpmapi.h)
author: windows-sdk-content
description: The IntServTspecBody structure contains information for an RSVP Tspec.
old-location: qos\intservtspecbody.htm
tech.root: QOS
ms.assetid: c4244dba-237a-437b-94b7-fd814edb3506
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IntServTspecBody, IntServTspecBody structure [QOS], lpmapi/IntServTspecBody, qos.intservtspecbody
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
ms.custom: 19H1
---

# IntServTspecBody structure


## -description


The 
<b>IntServTspecBody</b> structure contains information for an RSVP Tspec.


## -struct-fields




### -field st_mh

Header for the corresponding Tspec object, expressed as  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservmainhdr">IntServMainHdr</a> structure.


### -field tspec_u



#### gen_stspec

Generic Tspec, expressed as a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-gentspec">GenTspec</a> structure.



#### qual_stspec

Qualitative Tspec, expressed as a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-qualtspec">QualTspec</a> structure.


### -field gen_stspec

 


### -field qual_stspec

 




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-gentspec">GenTspec</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservmainhdr">IntServMainHdr</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-qualtspec">QualTspec</a>
 

 

