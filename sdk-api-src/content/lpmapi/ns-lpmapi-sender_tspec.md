---
UID: NS:lpmapi.SENDER_TSPEC
title: SENDER_TSPEC (lpmapi.h)
description: The SENDER_TSPEC structure contains information for an RSVP sender Tspec.
helpviewer_keywords: ["SENDER_TSPEC","SENDER_TSPEC structure [QOS]","lpmapi/SENDER_TSPEC","qos.sender_tspec"]
old-location: qos\sender_tspec.htm
tech.root: QOS
ms.assetid: d7905687-1af8-4469-b8de-a2445afa90f4
ms.date: 12/05/2018
ms.keywords: SENDER_TSPEC, SENDER_TSPEC structure [QOS], lpmapi/SENDER_TSPEC, qos.sender_tspec
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
req.typenames: SENDER_TSPEC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SENDER_TSPEC
 - lpmapi/SENDER_TSPEC
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
 - SENDER_TSPEC
---

# SENDER_TSPEC structure


## -description

The 
<b>SENDER_TSPEC</b> structure contains information for an RSVP sender Tspec.

## -struct-fields

### -field stspec_header

Object header, expressed as an <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-rsvpobjhdr">RsvpObjHdr</a> structure.

### -field stspec_body

Sender Tspec body information, expressed as an <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservtspecbody">IntServTspecBody</a> structure.

## -see-also

<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservtspecbody">IntServTspecBody</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-rsvpobjhdr">RsvpObjHdr</a>

