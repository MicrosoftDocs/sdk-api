---
UID: NS:qossp._RSVP_STATUS_INFO
title: RSVP_STATUS_INFO (qossp.h)
description: The QOS object RSVP_STATUS_INFO provides information regarding the status of RSVP for a given flow, including event notifications associated with monitoring FD_QOS events, as well as error information.
helpviewer_keywords: ["*LPRSVP_STATUS_INFO","LPRSVP_STATUS_INFO","LPRSVP_STATUS_INFO structure pointer [QOS]","RSVP_STATUS_INFO","RSVP_STATUS_INFO structure [QOS]","_gqos_rsvp_status_info","qos.rsvp_status_info","qossp/LPRSVP_STATUS_INFO","qossp/RSVP_STATUS_INFO"]
old-location: qos\rsvp_status_info.htm
tech.root: QOS
ms.assetid: ffb271e5-cdfe-4ac9-929e-9a0a81894238
ms.date: 12/05/2018
ms.keywords: '*LPRSVP_STATUS_INFO, LPRSVP_STATUS_INFO, LPRSVP_STATUS_INFO structure pointer [QOS], RSVP_STATUS_INFO, RSVP_STATUS_INFO structure [QOS], _gqos_rsvp_status_info, qos.rsvp_status_info, qossp/LPRSVP_STATUS_INFO, qossp/RSVP_STATUS_INFO'
req.header: qossp.h
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
req.typenames: RSVP_STATUS_INFO, *LPRSVP_STATUS_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RSVP_STATUS_INFO
 - qossp/_RSVP_STATUS_INFO
 - LPRSVP_STATUS_INFO
 - qossp/LPRSVP_STATUS_INFO
 - RSVP_STATUS_INFO
 - qossp/RSVP_STATUS_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Qossp.h
api_name:
 - RSVP_STATUS_INFO
---

# RSVP_STATUS_INFO structure


## -description

The QOS object 
<b>RSVP_STATUS_INFO</b> provides information regarding the status of RSVP for a given flow, including event notifications associated with monitoring FD_QOS events, as well as error information. 
<b>RSVP_STATUS_INFO</b> is useful for storing RSVP-specific status and error information.

## -struct-fields

### -field ObjectHdr

The QOS object 
<b>QOS_OBJECT_HDR</b>.

### -field StatusCode

Status information. See Winsock2.h for more information.

### -field ExtendedStatus1

Mechanism for storing or returning provider-specific status information. The <i>ExtendedStatus1</i> parameter is used for storing a higher-level, or generalized error code, and is augmented by finer-grained error information provided in ExtendedStatus2.

### -field ExtendedStatus2

Additional mechanism for storing or returning provider-specific status information. Provides finer-grained error information compared to the generalized error information provided in <i>ExtendedStatus1</i>.

## -remarks

When applications register their interest in FD_QOS events (see 
<a href="/previous-versions/aa374065(v=vs.80)">QOS Events</a>), event and error information is associated with the event in the form of the 
<a href="/windows/win32/api/winsock2/ns-winsock2-qos">QOS</a> structure that is associated with the event. For more detailed information associated with that event, applications can investigate the <b>RSVP_STATUS_INFO</b> object that is provided in 
<a href="/previous-versions/aa374467(v=vs.80)">the ProviderSpecific buffer</a> of the event-associated 
<b>QOS</b> structure.

## -see-also

<a href="/previous-versions/aa374467(v=vs.80)">ProviderSpecific Buffer</a>



<a href="/windows/win32/api/winsock2/ns-winsock2-qos">QOS</a>



<a href="/previous-versions/windows/desktop/api/qos/ns-qos-qos_object_hdr">QOS_OBJECT_HDR</a>