---
UID: NS:lpmapi.flow_desc
title: FLOW_DESC (lpmapi.h)
description: The FLOW_DESC structure contains flow descriptor information for RSVP.
helpviewer_keywords: ["FLOW_DESC","FLOW_DESC structure [QOS]","lpmapi/FLOW_DESC","qos.flow_desc"]
old-location: qos\flow_desc.htm
tech.root: QOS
ms.assetid: 11ecd7ac-13c4-4f55-9700-105153b4fead
ms.date: 12/05/2018
ms.keywords: FLOW_DESC, FLOW_DESC structure [QOS], lpmapi/FLOW_DESC, qos.flow_desc
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
req.typenames: FLOW_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - flow_desc
 - lpmapi/flow_desc
 - FLOW_DESC
 - lpmapi/FLOW_DESC
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
 - FLOW_DESC
---

# FLOW_DESC structure


## -description

The 
<b>FLOW_DESC</b> structure contains flow descriptor information for RSVP.

## -struct-fields

### -field u1

Union of Tspec and flowspec information.

### -field u1.stspec

Sender Tspec, expressed as a <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-sender_tspec">SENDER_TSPEC</a> structure.

### -field u1.isflow

Integrated Services flowspec information, expressed as an <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-is_flowspec">IS_FLOWSPEC</a> structure.

### -field u2

Union of sender and filterspec information.

### -field u2.stemp

Sender template for the flow, expressed as a <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-filter_spec">FILTER_SPEC</a> structure.

### -field u2.fspec

Filter spec for the flow, expressed as a <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-filter_spec">FILTER_SPEC</a> structure.

## -see-also

<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-filter_spec">FILTER_SPEC</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-is_flowspec">IS_FLOWSPEC</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-sender_tspec">SENDER_TSPEC</a>