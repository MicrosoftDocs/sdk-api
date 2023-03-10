---
UID: NS:lpmapi.CtrlLoadFlowspec
title: CtrlLoadFlowspec (lpmapi.h)
description: The CtrlLoadFlowspec structure contains a Controlled Load FLOWSPEC.
helpviewer_keywords: ["CtrlLoadFlowspec","CtrlLoadFlowspec structure [QOS]","lpmapi/CtrlLoadFlowspec","qos.ctrlloadflowspec"]
old-location: qos\ctrlloadflowspec.htm
tech.root: QOS
ms.assetid: def835ae-f0d2-4cdc-a498-315c4ef1245b
ms.date: 12/05/2018
ms.keywords: CtrlLoadFlowspec, CtrlLoadFlowspec structure [QOS], lpmapi/CtrlLoadFlowspec, qos.ctrlloadflowspec
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
req.typenames: CtrlLoadFlowspec
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CtrlLoadFlowspec
 - lpmapi/CtrlLoadFlowspec
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
 - CtrlLoadFlowspec
---

# CtrlLoadFlowspec structure


## -description

The 
<b>CtrlLoadFlowspec</b> structure contains a Controlled Load FLOWSPEC.

## -struct-fields

### -field CL_spec_serv_hdr

General information and length information for the controlled load flowspec object (this structure), expressed as an <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservservicehdr">IntServServiceHdr</a> structure.

### -field CL_spec_parm_hdr

Parameter header, expressed as an <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservparmhdr">IntServParmHdr</a> structure.

### -field CL_spec_parms

Generic Tspec  parameters, expressed as a <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-gentspecparms">GenTspecParms</a> structure.

## -see-also

<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-gentspecparms">GenTspecParms</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservparmhdr">IntServParmHdr</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservservicehdr">IntServServiceHdr</a>

