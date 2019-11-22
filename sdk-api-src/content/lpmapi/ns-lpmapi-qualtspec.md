---
UID: NS:lpmapi.__unnamed_struct_21
title: QualTspec (lpmapi.h)

description: The QualTspec structure contains qualitative Tspec information.
old-location: qos\qualtspec.htm
tech.root: QOS
ms.assetid: dc22de18-3e9f-4b92-aba4-579aa47fab64

ms.date: 12/05/2018
ms.keywords: QualTspec, QualTspec structure [QOS], lpmapi/QualTspec, qos.qualtspec
ms.topic: struct
f1_keywords: 
 - "lpmapi/QualTspec"
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
 - QualTspec
targetos: Windows
req.typenames: QualTspec
req.redist: 
ms.custom: 19H1
---

# QualTspec structure


## -description


The 
<b>QualTspec</b> structure contains qualitative Tspec information.


## -struct-fields




### -field qual_Tspec_serv_hdr

General information and length information for the QualTspec object (this structure), expressed as an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservservicehdr">IntServServiceHdr</a> structure.


### -field qual_Tspec_parm_hdr

Parameter header, expressed as an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservparmhdr">IntServParmHdr</a> structure.


### -field qual_Tspec_parms

Tspec parameters, expressed as a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-qualtspecparms">QualTspecParms</a> structure.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservparmhdr">IntServParmHdr</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservservicehdr">IntServServiceHdr</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-qualtspecparms">QualTspecParms</a>
 

 

