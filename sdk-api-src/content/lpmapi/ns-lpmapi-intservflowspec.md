---
UID: NS:lpmapi.IntServFlowSpec
title: IntServFlowSpec (lpmapi.h)
description: The IntServFlowSpec structure contains information about Integrated Services flowspecs.
helpviewer_keywords: ["IntServFlowSpec","IntServFlowSpec structure [QOS]","lpmapi/IntServFlowSpec","qos.intservflowspec"]
old-location: qos\intservflowspec.htm
tech.root: QOS
ms.assetid: c16115ba-03fa-4363-bf16-5341da54f792
ms.date: 12/05/2018
ms.keywords: IntServFlowSpec, IntServFlowSpec structure [QOS], lpmapi/IntServFlowSpec, qos.intservflowspec
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
req.typenames: IntServFlowSpec
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IntServFlowSpec
 - lpmapi/IntServFlowSpec
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
 - IntServFlowSpec
---

# IntServFlowSpec structure


## -description

The 
<b>IntServFlowSpec</b> structure contains information about Integrated Services flowspecs.

## -struct-fields

### -field spec_mh

General information and length information for the  flowspec object (this structure), expressed as an <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservmainhdr">IntServMainHdr</a> structure.

### -field spec_u

Union containing flowspec information.



#### CL_spec

Controlled load flowspec information, expressed as a <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-ctrlloadflowspec">CtrlLoadFlowspec</a> structure.



#### G_spec

Guaranteed service flowspec information, expressed as a <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-guarflowspec">GuarFlowSpec</a> structure.



#### Q_spec

Qualitative application flowspec information, expressed as a <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-qualappflowspec">QualAppFlowSpec</a> structure.

### -field CL_spec

### -field G_spec

### -field Q_spec

## -see-also

<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-ctrlloadflowspec">CtrlLoadFlowspec</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-guarflowspec">GuarFlowSpec</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-qualappflowspec">QualAppFlowSpec</a>

