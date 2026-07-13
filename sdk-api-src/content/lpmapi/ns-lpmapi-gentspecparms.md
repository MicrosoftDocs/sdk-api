---
UID: NS:lpmapi.GenTspecParms
title: GenTspecParms (lpmapi.h)
description: The GenTspecParms structure stores generic Tspec parameters.
helpviewer_keywords: ["GenTspecParms","GenTspecParms structure [QOS]","lpmapi/GenTspecParms","qos.gentspecparms"]
old-location: qos\gentspecparms.htm
tech.root: QOS
ms.assetid: 8a702e7c-0dfd-48f5-8612-d64d19f2a55c
ms.date: 12/05/2018
ms.keywords: GenTspecParms, GenTspecParms structure [QOS], lpmapi/GenTspecParms, qos.gentspecparms
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
req.typenames: GenTspecParms
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GenTspecParms
 - lpmapi/GenTspecParms
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
 - GenTspecParms
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

<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-gentspec">GenTspec</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservtspecbody">IntServTspecBody</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-qualappflowspec">QualAppFlowSpec</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-qualtspec">QualTspec</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-qualtspecparms">QualTspecParms</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-sender_tspec">SENDER_TSPEC</a>

