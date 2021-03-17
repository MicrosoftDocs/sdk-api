---
UID: NS:ifdef._IF_COUNTED_STRING_LH
title: IF_COUNTED_STRING_LH (ifdef.h)
description: The IF_COUNTED_STRING structure specifies a counted string for NDIS interfaces.
helpviewer_keywords: ["*PIF_COUNTED_STRING","*PIF_COUNTED_STRING_LH","IF_COUNTED_STRING","IF_COUNTED_STRING structure [Network Drivers Starting with Windows Vista]","IF_COUNTED_STRING_LH","PIF_COUNTED_STRING","PIF_COUNTED_STRING structure pointer [Network Drivers Starting with Windows Vista]","ifdef/IF_COUNTED_STRING","ifdef/PIF_COUNTED_STRING","netvista.if_counted_string"]
old-location: netvista\if_counted_string.htm
tech.root: NetVista
ms.assetid: 44B59154-C5CA-42F0-A972-021833E29D81
ms.date: 12/05/2018
ms.keywords: '*PIF_COUNTED_STRING, *PIF_COUNTED_STRING_LH, IF_COUNTED_STRING, IF_COUNTED_STRING structure [Network Drivers Starting with Windows Vista], IF_COUNTED_STRING_LH, PIF_COUNTED_STRING, PIF_COUNTED_STRING structure pointer [Network Drivers Starting with Windows Vista], ifdef/IF_COUNTED_STRING, ifdef/PIF_COUNTED_STRING, netvista.if_counted_string'
req.header: ifdef.h
req.include-header: Ntddndis.h
req.target-type: Windows
req.target-min-winverclnt: Supported in NDIS 6.0 and later.
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
req.typenames: IF_COUNTED_STRING_LH, *PIF_COUNTED_STRING_LH
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IF_COUNTED_STRING_LH
 - ifdef/_IF_COUNTED_STRING_LH
 - PIF_COUNTED_STRING_LH
 - ifdef/PIF_COUNTED_STRING_LH
 - IF_COUNTED_STRING_LH
 - ifdef/IF_COUNTED_STRING_LH
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ifdef.h
api_name:
 - IF_COUNTED_STRING
---

# IF_COUNTED_STRING_LH structure


## -description

The <b>IF_COUNTED_STRING</b> structure specifies a counted string for NDIS interfaces.

## -struct-fields

### -field Length

A USHORT value that contains the length, in bytes, of the string.

### -field String

A WCHAR buffer that contains the string. The string does not need to be null-terminated.

## -remarks

The <b>IF_COUNTED_STRING</b> structure is the data type for various NDIS string structures, such as <b>NDIS_IF_COUNTED_STRING</b>.

If the string is NULL-terminated, the <b>Length</b> member must not include the terminating NULL character.

