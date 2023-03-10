---
UID: NS:lpmapi.rsvpmsgobjs
title: RSVP_MSG_OBJS (lpmapi.h)
description: The RSVP_MSG_OBJS structure contains RSVP message objects.
helpviewer_keywords: ["RSVP_MSG_OBJS","RSVP_MSG_OBJS structure [QOS]","lpmapi/RSVP_MSG_OBJS","qos.rsvp_msg_objs"]
old-location: qos\rsvp_msg_objs.htm
tech.root: QOS
ms.assetid: 4ca0bfbc-7c1b-4395-b0fb-487e5c36b5d8
ms.date: 12/05/2018
ms.keywords: RSVP_MSG_OBJS, RSVP_MSG_OBJS structure [QOS], lpmapi/RSVP_MSG_OBJS, qos.rsvp_msg_objs
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
req.typenames: RSVP_MSG_OBJS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - rsvpmsgobjs
 - lpmapi/rsvpmsgobjs
 - RSVP_MSG_OBJS
 - lpmapi/RSVP_MSG_OBJS
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
 - RSVP_MSG_OBJS
---

# RSVP_MSG_OBJS structure


## -description

The 
<b>RSVP_MSG_OBJS</b> structure contains RSVP message objects.

## -struct-fields

### -field RsvpMsgType

RSVP message type.

### -field pRsvpSession

Pointer to an <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-rsvp_session">RSVP_SESSION</a> object containing an RSVP session object.

### -field pRsvpFromHop

Pointer to an <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-rsvp_hop">RSVP_HOP</a> structure indicating the hop from which the message has come.

### -field pRsvpToHop

Pointer to an <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-rsvp_hop">RSVP_HOP</a> structure indicating the hop to which the message shall be sent.

### -field pResvStyle

Reservation style, expressed as a <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-resv_style">RESV_STYLE</a> structure.

### -field pRsvpScope

Scope of the reservation message.

### -field FlowDescCount

Number of flow descriptors in the message.

### -field pFlowDescs

Pointer to the first <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-flow_desc">FLOW_DESC</a> structure in the message.

### -field PdObjectCount

Number of policy data objects in the message.

### -field ppPdObjects

Pointer to the first <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-policy_data">POLICY_DATA</a> structure in the message.

### -field pErrorSpec

Pointer to an <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-error_spec">ERROR_SPEC</a> structure containing an error message.

### -field pAdspec

Pointer to an <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-adspec">ADSPEC</a> structure containing an Adspec message.

## -see-also

<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-adspec">ADSPEC</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-error_spec">ERROR_SPEC</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-flow_desc">FLOW_DESC</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-policy_data">POLICY_DATA</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-resv_style">RESV_STYLE</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-rsvp_hop">RSVP_HOP</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-rsvp_session">RSVP_SESSION</a>