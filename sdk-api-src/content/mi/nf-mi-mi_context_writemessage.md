---
UID: NF:mi.MI_Context_WriteMessage
title: MI_Context_WriteMessage function (mi.h)
description: Sends an operational message to the client.
helpviewer_keywords: ["MI_Context_WriteMessage","MI_Context_WriteMessage function [Windows Management Infrastructure (MI)]","MI_WRITEMESSAGE_CHANNEL_DEBUG","MI_WRITEMESSAGE_CHANNEL_VERBOSE","MI_WRITEMESSAGE_CHANNEL_WARNING","mi/MI_Context_WriteMessage","wmi.mi_writemessage","wmi_v2.mi_context_writemessage"]
old-location: wmi_v2\mi_context_writemessage.htm
tech.root: wmi_v2
ms.assetid: 2e4dbb4d-5482-4ed0-9903-34b3bb87b16f
ms.date: 12/05/2018
ms.keywords: MI_Context_WriteMessage, MI_Context_WriteMessage function [Windows Management Infrastructure (MI)], MI_WRITEMESSAGE_CHANNEL_DEBUG, MI_WRITEMESSAGE_CHANNEL_VERBOSE, MI_WRITEMESSAGE_CHANNEL_WARNING, mi/MI_Context_WriteMessage, wmi.mi_writemessage, wmi_v2.mi_context_writemessage
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
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - MI_Context_WriteMessage
 - mi/MI_Context_WriteMessage
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
 - MI_Context_WriteMessage
---

# MI_Context_WriteMessage function


## -description

Sends an operational message to the client.

## -parameters

### -param context [in]

Request context.

### -param channel

The channel to which to write.  The client can select from one these channels:



#### MI_WRITEMESSAGE_CHANNEL_WARNING (0)

Channel used to broadcast warning messages.



#### MI_WRITEMESSAGE_CHANNEL_VERBOSE (1)

Channel used to broadcast verbose informational messages.



#### MI_WRITEMESSAGE_CHANNEL_DEBUG (2)

Channel used to broadcast debugging information.

### -param message

A null-terminated string that represents the message to be sent to the client. The message should be localized if it is a warning or verbose.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -remarks

A provider calls this function  when an operational message needs to be sent to the client about something.  An example of an operational message would be notifying the client as to which files have been deleted in a long running delete process so that the client can update the UI. Care should be taken not to overuse this function as it can slow down the progress of the provider.  A client can optionally register to receive these messages via an asynchronous callback.  If a client does not register for these messages, the server will ignore the message.

## -see-also

<a href="/windows/desktop/api/mi/ns-mi-mi_context">MI_Context</a>