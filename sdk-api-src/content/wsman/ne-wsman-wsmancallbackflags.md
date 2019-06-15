---
UID: NE:wsman.WSManCallbackFlags
title: WSManCallbackFlags (wsman.h)
author: windows-sdk-content
description: Defines a set of flags used by all callback functions.
old-location: winrm\wsmancallbackflags.htm
tech.root: winrm
ms.assetid: ce4c664d-bc69-415a-955d-7761f58a25e2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WSMAN_FLAG_CALLBACK_END_OF_OPERATION, WSMAN_FLAG_CALLBACK_END_OF_STREAM, WSManCallbackFlags, WSManCallbackFlags enumeration [Windows Remote Management], winrm.wsmancallbackflags, wsman/WSMAN_FLAG_CALLBACK_END_OF_OPERATION, wsman/WSMAN_FLAG_CALLBACK_END_OF_STREAM, wsman/WSManCallbackFlags
ms.topic: enum
f1_keywords: ["wsman/WSManCallbackFlags"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wsman.h
api_name:
 - WSManCallbackFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework on Windows Server 2008 with SP2 and Windows Vista with SP2
ms.custom: 19H1
---

# WSManCallbackFlags enumeration


## -description


Defines a set of flags used by all callback functions.


## -enum-fields




### -field WSMAN_FLAG_CALLBACK_END_OF_OPERATION

Indicates the end of a single step of a multi-step operation. This flag is used for optimization purposes if the shell cannot be determined.


### -field WSMAN_FLAG_CALLBACK_END_OF_STREAM

Indicates the end of a particular stream. This flag is used for optimization purposes if an indication has been provided to the shell that no more output will occur for this stream.


### -field WSMAN_FLAG_CALLBACK_SHELL_SUPPORTS_DISCONNECT


### -field WSMAN_FLAG_CALLBACK_SHELL_AUTODISCONNECTED


### -field WSMAN_FLAG_CALLBACK_NETWORK_FAILURE_DETECTED


### -field WSMAN_FLAG_CALLBACK_RETRYING_AFTER_NETWORK_FAILURE


### -field WSMAN_FLAG_CALLBACK_RECONNECTED_AFTER_NETWORK_FAILURE


### -field WSMAN_FLAG_CALLBACK_SHELL_AUTODISCONNECTING


### -field WSMAN_FLAG_CALLBACK_RETRY_ABORTED_DUE_TO_INTERNAL_ERROR


### -field WSMAN_FLAG_CALLBACK_RECEIVE_DELAY_STREAM_REQUEST_PROCESSED



