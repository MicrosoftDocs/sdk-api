---
UID: NS:lpmapi.__unnamed_struct_19
title: GenTspec (lpmapi.h)
author: windows-sdk-content
description: The GenTspec structure stores generic Tspec information.
old-location: qos\gentspec.htm
tech.root: QOS
ms.assetid: cefd94ed-ed54-471d-97fc-d523cedd71d6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GenTspec, GenTspec structure [QOS], lpmapi/GenTspec, qos.gentspec
ms.topic: struct
f1_keywords: 
 - "lpmapi/GenTspec"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: GenTspec
req.redist: 
ms.custom: 19H1
---

# GenTspec structure


## -description


The 
<b>GenTspec</b> structure stores generic Tspec information.


## -struct-fields




### -field gen_Tspec_serv_hdr

General information and length information for the GenTspec object (this structure), expressed as an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservservicehdr">IntServServiceHdr</a> structure.


### -field gen_Tspec_parm_hdr

Parameter header, expressed as an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservparmhdr">IntServParmHdr</a> structure.


### -field gen_Tspec_parms

Tspec parameters, expressed as a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-gentspecparms">GenTspecParms</a> structure.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-gentspecparms">GenTspecParms</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservparmhdr">IntServParmHdr</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservservicehdr">IntServServiceHdr</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservtspecbody">IntServTspecBody</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-qualappflowspec">QualAppFlowSpec</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-qualtspec">QualTspec</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-qualtspecparms">QualTspecParms</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-sender_tspec">SENDER_TSPEC</a>
 

 

