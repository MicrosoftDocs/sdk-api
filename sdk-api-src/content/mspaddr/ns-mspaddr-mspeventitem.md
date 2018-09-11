---
UID: NS:mspaddr.MSPEVENTITEM
title: MSPEVENTITEM
author: windows-sdk-content
description: The MSPEVENTITEM structure contains link pointers and event types for MSP events.
old-location: tapi3\mspeventitem.htm
tech.root: tapi
ms.assetid: fc99fd05-4d87-4b6e-b2f3-e00ac61ddafc
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: "*PMSPEVENTITEM, MSPEVENTITEM, MSPEVENTITEM structure [TAPI 2.2], PMSPEVENTITEM, PMSPEVENTITEM structure pointer [TAPI 2.2], _tapi3_mspeventitem, mspaddr/MSPEVENTITEM, mspaddr/PMSPEVENTITEM, tapi3.mspeventitem"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mspaddr.h
api_name:
 - MSPEVENTITEM
product: Windows
targetos: Windows
req.typenames: MSPEVENTITEM, *PMSPEVENTITEM
req.redist: 
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
<a href="https://msdn.microsoft.com/5286fbe6-3553-42f1-82e6-5bb6f75f3305">MSP_EVENT_INFO</a> structure contains information concerning an event.

