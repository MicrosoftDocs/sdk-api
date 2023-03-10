---
UID: NE:wsman.WSManCallbackFlags
title: WSManCallbackFlags (wsman.h)
description: Defines a set of flags used by all callback functions.
helpviewer_keywords: ["WSMAN_FLAG_CALLBACK_END_OF_OPERATION","WSMAN_FLAG_CALLBACK_END_OF_STREAM","WSManCallbackFlags","WSManCallbackFlags enumeration [Windows Remote Management]","winrm.wsmancallbackflags","wsman/WSMAN_FLAG_CALLBACK_END_OF_OPERATION","wsman/WSMAN_FLAG_CALLBACK_END_OF_STREAM","wsman/WSManCallbackFlags"]
old-location: winrm\wsmancallbackflags.htm
tech.root: winrm
ms.assetid: ce4c664d-bc69-415a-955d-7761f58a25e2
ms.date: 12/05/2018
ms.keywords: WSMAN_FLAG_CALLBACK_END_OF_OPERATION, WSMAN_FLAG_CALLBACK_END_OF_STREAM, WSManCallbackFlags, WSManCallbackFlags enumeration [Windows Remote Management], winrm.wsmancallbackflags, wsman/WSMAN_FLAG_CALLBACK_END_OF_OPERATION, wsman/WSMAN_FLAG_CALLBACK_END_OF_STREAM, wsman/WSManCallbackFlags
req.header: wsman.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
req.typenames: 
req.redist: Windows Management Framework on Windows Server 2008 with SP2 and Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - WSManCallbackFlags
 - wsman/WSManCallbackFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wsman.h
api_name:
 - WSManCallbackFlags
---

# WSManCallbackFlags enumeration


## -description

Defines a set of flags used by all callback functions.

## -enum-fields

### -field WSMAN_FLAG_CALLBACK_END_OF_OPERATION:0x1

Indicates the end of a single step of a multi-step operation. This flag is used for optimization purposes if the shell cannot be determined.

### -field WSMAN_FLAG_CALLBACK_END_OF_STREAM:0x8

Indicates the end of a particular stream. This flag is used for optimization purposes if an indication has been provided to the shell that no more output will occur for this stream.

### -field WSMAN_FLAG_CALLBACK_SHELL_SUPPORTS_DISCONNECT:0x20

### -field WSMAN_FLAG_CALLBACK_SHELL_AUTODISCONNECTED:0x40

### -field WSMAN_FLAG_CALLBACK_NETWORK_FAILURE_DETECTED:0x100

### -field WSMAN_FLAG_CALLBACK_RETRYING_AFTER_NETWORK_FAILURE:0x200

### -field WSMAN_FLAG_CALLBACK_RECONNECTED_AFTER_NETWORK_FAILURE:0x400

### -field WSMAN_FLAG_CALLBACK_SHELL_AUTODISCONNECTING:0x800

### -field WSMAN_FLAG_CALLBACK_RETRY_ABORTED_DUE_TO_INTERNAL_ERROR:0x1000

### -field WSMAN_FLAG_CALLBACK_RECEIVE_DELAY_STREAM_REQUEST_PROCESSED:0X2000

