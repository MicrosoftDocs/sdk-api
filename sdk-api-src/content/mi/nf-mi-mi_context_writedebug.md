---
UID: NF:mi.MI_Context_WriteDebug
title: MI_Context_WriteDebug function (mi.h)
description: Sends a debug message to the client.
helpviewer_keywords: ["MI_Context_WriteDebug","MI_Context_WriteDebug function [Windows Management Infrastructure (MI)]","mi/MI_Context_WriteDebug","wmi.mi_writedebug","wmi_v2.mi_context_writedebug"]
old-location: wmi_v2\mi_context_writedebug.htm
tech.root: wmi_v2
ms.assetid: 07413425-bc4a-46d7-8ed8-121eafab97cc
ms.date: 12/05/2018
ms.keywords: MI_Context_WriteDebug, MI_Context_WriteDebug function [Windows Management Infrastructure (MI)], mi/MI_Context_WriteDebug, wmi.mi_writedebug, wmi_v2.mi_context_writedebug
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
 - MI_Context_WriteDebug
 - mi/MI_Context_WriteDebug
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
 - MI_Context_WriteDebug
---

# MI_Context_WriteDebug function


## -description

Sends a debug message to the client.

## -parameters

### -param context [in]

Request context

### -param message

A null-terminated string that represents the debug message to send to the client. Localizing the message is optional, but recommended.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -remarks

A provider calls this function  when a debug message needs to be sent to the client.  Debug messages can be useful in determining why a given action is not completing successfully. A client can optionally register to receive these messages via an asynchronous callback.  If a client does not register for these messages, the server will ignore the message.