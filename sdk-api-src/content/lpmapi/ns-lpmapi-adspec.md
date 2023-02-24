---
UID: NS:lpmapi.ADSPEC
title: ADSPEC (lpmapi.h)
description: The ADSPEC structure contains Adspec message information for RSVP.
helpviewer_keywords: ["ADSPEC","ADSPEC structure [QOS]","lpmapi/ADSPEC","qos.adspec"]
old-location: qos\adspec.htm
tech.root: QOS
ms.assetid: c5be3864-0f21-4fa5-99f8-dee9ad2b7286
ms.date: 12/05/2018
ms.keywords: ADSPEC, ADSPEC structure [QOS], lpmapi/ADSPEC, qos.adspec
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
req.typenames: ADSPEC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ADSPEC
 - lpmapi/ADSPEC
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
 - ADSPEC
---

# ADSPEC structure


## -description

The 
<b>ADSPEC</b> structure contains Adspec message information for RSVP.

## -struct-fields

### -field adspec_header

Adspec header, expressed as an <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-rsvpobjhdr">RsvpObjHdr</a> structure.

### -field adspec_body

Adspec message body.

## -see-also

<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-rsvpobjhdr">RsvpObjHdr</a>

