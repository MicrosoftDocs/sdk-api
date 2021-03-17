---
UID: NF:mi.MI_Context_WriteWarning
title: MI_Context_WriteWarning function (mi.h)
description: Writes a warning message to the client.
helpviewer_keywords: ["MI_Context_WriteWarning","MI_Context_WriteWarning function [Windows Management Infrastructure (MI)]","mi/MI_Context_WriteWarning","wmi.mi_writewarning","wmi_v2.mi_context_writewarning"]
old-location: wmi_v2\mi_context_writewarning.htm
tech.root: wmi_v2
ms.assetid: b353eff6-2d62-4dfc-8a21-bf21cf2f6437
ms.date: 12/05/2018
ms.keywords: MI_Context_WriteWarning, MI_Context_WriteWarning function [Windows Management Infrastructure (MI)], mi/MI_Context_WriteWarning, wmi.mi_writewarning, wmi_v2.mi_context_writewarning
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
 - MI_Context_WriteWarning
 - mi/MI_Context_WriteWarning
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
 - MI_Context_WriteWarning
---

# MI_Context_WriteWarning function


## -description

Writes a warning message to the client.

## -parameters

### -param context [in]

Request context

### -param message

A null-terminated string representing a warning message to send to client. This string should be localized.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -remarks

Warning messages should warn of exceptional circumstances.  The client can optionally register to receive these messages via an asynchronous callback.  If a client does not register for these messages, the server will ignore the message.