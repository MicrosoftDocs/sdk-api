---
UID: NS:lpmapi.__unnamed_struct_22
title: QualAppFlowSpec (lpmapi.h)
author: windows-sdk-content
description: The QualAppFlowSpec structure contains FLOWSPEC information for a qualitative application.
old-location: qos\qualappflowspec.htm
tech.root: QOS
ms.assetid: 4e15b094-4250-4699-b66e-6734cf37cbb6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: QualAppFlowSpec, QualAppFlowSpec structure [QOS], lpmapi/QualAppFlowSpec, qos.qualappflowspec
ms.topic: struct
f1_keywords: ["lpmapi/QualAppFlowSpec"]
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
ms.custom: 19H1
---

# QualAppFlowSpec structure


## -description


The 
<b>QualAppFlowSpec</b> structure contains FLOWSPEC information for a qualitative application.


## -struct-fields




### -field Q_spec_serv_hdr

General information and length information for the QualAppFlowSpec object (this structure), expressed as an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservservicehdr">IntServServiceHdr</a> structure.


### -field Q_spec_parm_hdr

Parameter header, expressed as an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservparmhdr">IntServParmHdr</a> structure.


### -field Q_spec_parms

QUALITATIVE Tspec parameters, expressed as a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-qualtspecparms">QualTspecParms</a> structure.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservparmhdr">IntServParmHdr</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservservicehdr">IntServServiceHdr</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-qualtspecparms">QualTspecParms</a>
 

 

