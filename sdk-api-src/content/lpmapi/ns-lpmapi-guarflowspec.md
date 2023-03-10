---
UID: NS:lpmapi.GuarFlowSpec
title: GuarFlowSpec (lpmapi.h)
description: The GuarFlowSpec structure contains guaranteed flowspec information.
helpviewer_keywords: ["GuarFlowSpec","GuarFlowSpec structure [QOS]","lpmapi/GuarFlowSpec","qos.guarflowspec"]
old-location: qos\guarflowspec.htm
tech.root: QOS
ms.assetid: 549380cc-b4ac-414a-9058-f506741f1e76
ms.date: 12/05/2018
ms.keywords: GuarFlowSpec, GuarFlowSpec structure [QOS], lpmapi/GuarFlowSpec, qos.guarflowspec
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
targetos: Windows
req.typenames: GuarFlowSpec
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GuarFlowSpec
 - lpmapi/GuarFlowSpec
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lpmapi.h
api_name:
 - GuarFlowSpec
---

# GuarFlowSpec structure


## -description

The 
<b>GuarFlowSpec</b> structure contains guaranteed flowspec information.

## -struct-fields

### -field Guar_serv_hdr

General information and length information for the guaranteed flowspec object (this structure), expressed as an <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservservicehdr">IntServServiceHdr</a> structure.

### -field Guar_Tspec_hdr

Parameter header for the guaranteed Tspec, expressed as an <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservparmhdr">IntServParmHdr</a> structure.

### -field Guar_Tspec_parms

Generic Tspec  parameters, expressed as a <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-gentspecparms">GenTspecParms</a> structure.

### -field Guar_Rspec_hdr

Parameter header for the guaranteed Rspec, expressed as an <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservparmhdr">IntServParmHdr</a> structure.

### -field Guar_Rspec

Guaranteed rate, in bytes per second, expressed as a <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-guarrspec">GuarRspec</a> structure.

## -see-also

<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-gentspecparms">GenTspecParms</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-guarrspec">GuarRspec</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservparmhdr">IntServParmHdr</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservservicehdr">IntServServiceHdr</a>

