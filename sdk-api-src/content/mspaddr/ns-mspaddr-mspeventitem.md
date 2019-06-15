---
UID: NS:mspaddr.__unnamed_struct_0
title: MSPEVENTITEM (mspaddr.h)
author: windows-sdk-content
description: The MSPEVENTITEM structure contains link pointers and event types for MSP events.
old-location: tapi3\mspeventitem.htm
tech.root: Tapi
ms.assetid: fc99fd05-4d87-4b6e-b2f3-e00ac61ddafc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PMSPEVENTITEM, MSPEVENTITEM, MSPEVENTITEM structure [TAPI 2.2], PMSPEVENTITEM, PMSPEVENTITEM structure pointer [TAPI 2.2], _tapi3_mspeventitem, mspaddr/MSPEVENTITEM, mspaddr/PMSPEVENTITEM, tapi3.mspeventitem"
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
ms.custom: 19H1
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
<a href="https://docs.microsoft.com/windows/desktop/api/msp/ns-msp-__midl___midl_itf_msp_0000_0000_0005">MSP_EVENT_INFO</a> structure contains information concerning an event.

