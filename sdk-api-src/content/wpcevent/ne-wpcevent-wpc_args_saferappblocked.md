---
UID: NE:wpcevent.tagWPC_ARGS_SAFERAPPBLOCKED
title: WPC_ARGS_SAFERAPPBLOCKED (wpcevent.h)
description: Indicates information about a safer application that is being blocked.
helpviewer_keywords: ["WPC_ARGS_SAFERAPPBLOCKED","WPC_ARGS_SAFERAPPBLOCKED enumeration","WPC_ARGS_SAFERAPPBLOCKED_CARGS","WPC_ARGS_SAFERAPPBLOCKED_PATH","WPC_ARGS_SAFERAPPBLOCKED_RULEID","WPC_ARGS_SAFERAPPBLOCKED_TIMESTAMP","WPC_ARGS_SAFERAPPBLOCKED_USERID","parcon.wpc_args_saferappblocked","wpcevent/WPC_ARGS_SAFERAPPBLOCKED","wpcevent/WPC_ARGS_SAFERAPPBLOCKED_CARGS","wpcevent/WPC_ARGS_SAFERAPPBLOCKED_PATH","wpcevent/WPC_ARGS_SAFERAPPBLOCKED_RULEID","wpcevent/WPC_ARGS_SAFERAPPBLOCKED_TIMESTAMP","wpcevent/WPC_ARGS_SAFERAPPBLOCKED_USERID"]
old-location: parcon\wpc_args_saferappblocked.htm
tech.root: parcon
ms.assetid: 8fdc7d09-6bbb-4e0b-82f5-276186312f75
ms.date: 12/05/2018
ms.keywords: WPC_ARGS_SAFERAPPBLOCKED, WPC_ARGS_SAFERAPPBLOCKED enumeration, WPC_ARGS_SAFERAPPBLOCKED_CARGS, WPC_ARGS_SAFERAPPBLOCKED_PATH, WPC_ARGS_SAFERAPPBLOCKED_RULEID, WPC_ARGS_SAFERAPPBLOCKED_TIMESTAMP, WPC_ARGS_SAFERAPPBLOCKED_USERID, parcon.wpc_args_saferappblocked, wpcevent/WPC_ARGS_SAFERAPPBLOCKED, wpcevent/WPC_ARGS_SAFERAPPBLOCKED_CARGS, wpcevent/WPC_ARGS_SAFERAPPBLOCKED_PATH, wpcevent/WPC_ARGS_SAFERAPPBLOCKED_RULEID, wpcevent/WPC_ARGS_SAFERAPPBLOCKED_TIMESTAMP, wpcevent/WPC_ARGS_SAFERAPPBLOCKED_USERID
req.header: wpcevent.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: WPC_ARGS_SAFERAPPBLOCKED
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagWPC_ARGS_SAFERAPPBLOCKED
 - wpcevent/tagWPC_ARGS_SAFERAPPBLOCKED
 - WPC_ARGS_SAFERAPPBLOCKED
 - wpcevent/WPC_ARGS_SAFERAPPBLOCKED
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wpcevent.h
api_name:
 - WPC_ARGS_SAFERAPPBLOCKED
---

# WPC_ARGS_SAFERAPPBLOCKED enumeration


## -description

Indicates information about a safer application that is being blocked.

## -enum-fields

### -field WPC_ARGS_SAFERAPPBLOCKED_TIMESTAMP:0

The time stamp for the blocked application.

### -field WPC_ARGS_SAFERAPPBLOCKED_USERID

The user identifier of the blocked application.

### -field WPC_ARGS_SAFERAPPBLOCKED_PATH

The location of the blocked application.

### -field WPC_ARGS_SAFERAPPBLOCKED_RULEID

The rule identifier of the blocked application.

### -field WPC_ARGS_SAFERAPPBLOCKED_CARGS

The arguments of the blocked application.

