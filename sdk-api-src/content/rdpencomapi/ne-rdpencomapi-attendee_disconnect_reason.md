---
UID: NE:rdpencomapi.__MIDL___MIDL_itf_rdpencomapi_0000_0000_0002
title: ATTENDEE_DISCONNECT_REASON (rdpencomapi.h)
description: Defines values for the reasons why an attendee was disconnected from the session.
helpviewer_keywords: ["ATTENDEE_DISCONNECT_REASON","ATTENDEE_DISCONNECT_REASON enumeration [RDP]","ATTENDEE_DISCONNECT_REASON_APP","ATTENDEE_DISCONNECT_REASON_CLI","ATTENDEE_DISCONNECT_REASON_ERR","ATTENDEE_DISCONNECT_REASON_MAX","ATTENDEE_DISCONNECT_REASON_MIN","rdp.attendee_disconnect_reason","rdpencomapi/ATTENDEE_DISCONNECT_REASON","rdpencomapi/ATTENDEE_DISCONNECT_REASON_APP","rdpencomapi/ATTENDEE_DISCONNECT_REASON_CLI","rdpencomapi/ATTENDEE_DISCONNECT_REASON_ERR","rdpencomapi/ATTENDEE_DISCONNECT_REASON_MAX","rdpencomapi/ATTENDEE_DISCONNECT_REASON_MIN"]
old-location: rdp\attendee_disconnect_reason.htm
tech.root: rdp
ms.assetid: 2fbe5df8-54da-49b2-a9b8-275e838c6d39
ms.date: 12/05/2018
ms.keywords: ATTENDEE_DISCONNECT_REASON, ATTENDEE_DISCONNECT_REASON enumeration [RDP], ATTENDEE_DISCONNECT_REASON_APP, ATTENDEE_DISCONNECT_REASON_CLI, ATTENDEE_DISCONNECT_REASON_ERR, ATTENDEE_DISCONNECT_REASON_MAX, ATTENDEE_DISCONNECT_REASON_MIN, rdp.attendee_disconnect_reason, rdpencomapi/ATTENDEE_DISCONNECT_REASON, rdpencomapi/ATTENDEE_DISCONNECT_REASON_APP, rdpencomapi/ATTENDEE_DISCONNECT_REASON_CLI, rdpencomapi/ATTENDEE_DISCONNECT_REASON_ERR, rdpencomapi/ATTENDEE_DISCONNECT_REASON_MAX, rdpencomapi/ATTENDEE_DISCONNECT_REASON_MIN
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rdpencomapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ATTENDEE_DISCONNECT_REASON
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_rdpencomapi_0000_0000_0002
 - rdpencomapi/__MIDL___MIDL_itf_rdpencomapi_0000_0000_0002
 - ATTENDEE_DISCONNECT_REASON
 - rdpencomapi/ATTENDEE_DISCONNECT_REASON
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rdpencomapi.h
api_name:
 - ATTENDEE_DISCONNECT_REASON
---

# ATTENDEE_DISCONNECT_REASON enumeration


## -description

Defines values for the reasons why an attendee was disconnected from the session.

## -enum-fields

### -field ATTENDEE_DISCONNECT_REASON_MIN:0

Minimum enumeration value.

### -field ATTENDEE_DISCONNECT_REASON_APP:0

The application called the <a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiattendee-terminateconnection">IRDPSRAPIAttendee::TerminateConnection</a> method.

### -field ATTENDEE_DISCONNECT_REASON_ERR:1

There was an internal error when processing data from an attendee or trying to manage an attendee

### -field ATTENDEE_DISCONNECT_REASON_CLI:2

The attendee disconnected after a request from the attendee itself.

### -field ATTENDEE_DISCONNECT_REASON_MAX:2

Maximum enumeration value.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiattendeedisconnectinfo-get_reason">Reason Property of IRDPSRAPIAttendeeDisconnectInfo</a>
