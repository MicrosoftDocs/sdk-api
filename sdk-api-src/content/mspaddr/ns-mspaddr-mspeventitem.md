---
UID: NS:mspaddr.MSPEVENTITEM
title: MSPEVENTITEM (mspaddr.h)
description: The MSPEVENTITEM structure contains link pointers and event types for MSP events.
helpviewer_keywords: ["*PMSPEVENTITEM","MSPEVENTITEM","MSPEVENTITEM structure [TAPI 2.2]","PMSPEVENTITEM","PMSPEVENTITEM structure pointer [TAPI 2.2]","_tapi3_mspeventitem","mspaddr/MSPEVENTITEM","mspaddr/PMSPEVENTITEM","tapi3.mspeventitem"]
old-location: tapi3\mspeventitem.htm
tech.root: tapi3
ms.assetid: fc99fd05-4d87-4b6e-b2f3-e00ac61ddafc
ms.date: 12/05/2018
ms.keywords: '*PMSPEVENTITEM, MSPEVENTITEM, MSPEVENTITEM structure [TAPI 2.2], PMSPEVENTITEM, PMSPEVENTITEM structure pointer [TAPI 2.2], _tapi3_mspeventitem, mspaddr/MSPEVENTITEM, mspaddr/PMSPEVENTITEM, tapi3.mspeventitem'
req.header: mspaddr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: MSPEVENTITEM, *PMSPEVENTITEM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PMSPEVENTITEM
 - mspaddr/PMSPEVENTITEM
 - MSPEVENTITEM
 - mspaddr/MSPEVENTITEM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mspaddr.h
api_name:
 - MSPEVENTITEM
---

# MSPEVENTITEM structure


## -description

The 
<b>MSPEVENTITEM</b> structure contains link pointers and event types for MSP events.

## -struct-fields

### -field Link

Doubly-linked list. Part of Windows 2000 run-time routines that are callable by both kernel mode code in the executive and user mode code in various subsystems. See Ntrtl.h or search the Platform SDK for details.

### -field MSPEventInfo

The 
<a href="/windows/win32/api/msp/ns-msp-msp_event_info">MSP_EVENT_INFO</a> structure contains information concerning an event.

