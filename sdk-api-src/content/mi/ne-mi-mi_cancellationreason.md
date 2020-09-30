---
UID: NE:mi._MI_CancellationReason
title: MI_CancellationReason (mi.h)
description: Value to pass to an operation cancel request to notify the system of the reason the operation is being canceled. If the service is being shutdown, it may pass one of these values to the provider as well.
helpviewer_keywords: ["MI_CancellationReason","MI_CancellationReason enumeration [Windows Management Infrastructure (MI)]","MI_REASON_NONE","MI_REASON_SERVICESTOP","MI_REASON_SHUTDOWN","MI_REASON_TIMEOUT","mi/MI_CancellationReason","mi/MI_REASON_NONE","mi/MI_REASON_SERVICESTOP","mi/MI_REASON_SHUTDOWN","mi/MI_REASON_TIMEOUT","wmi._mi_cancellationreason","wmi_v2.mi_cancellationreason"]
old-location: wmi_v2\mi_cancellationreason.htm
tech.root: wmi_v2
ms.assetid: 3c498055-03ef-4163-9de5-cf4e70051cea
ms.date: 12/05/2018
ms.keywords: MI_CancellationReason, MI_CancellationReason enumeration [Windows Management Infrastructure (MI)], MI_REASON_NONE, MI_REASON_SERVICESTOP, MI_REASON_SHUTDOWN, MI_REASON_TIMEOUT, mi/MI_CancellationReason, mi/MI_REASON_NONE, mi/MI_REASON_SERVICESTOP, mi/MI_REASON_SHUTDOWN, mi/MI_REASON_TIMEOUT, wmi._mi_cancellationreason, wmi_v2.mi_cancellationreason
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
req.typenames: MI_CancellationReason
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_CancellationReason
 - mi/_MI_CancellationReason
 - MI_CancellationReason
 - mi/MI_CancellationReason
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_CancellationReason
---

# MI_CancellationReason enumeration


## -description

Value to pass to an operation cancel request to notify the system of the reason the operation is being canceled.  If the service is being shutdown, it may pass one of these values to the provider as well.

## -enum-fields

### -field MI_REASON_NONE

No reason for cancellation.

### -field MI_REASON_TIMEOUT

Operation timed out.

### -field MI_REASON_SHUTDOWN

The system is being shutdown.

### -field MI_REASON_SERVICESTOP

The service is being stopped.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dn792316(v=vs.85)">MI_CancelCallback</a>