---
UID: NF:mi.MI_Context_WriteVerbose
title: MI_Context_WriteVerbose function (mi.h)
description: Writes a verbose message to the client.
helpviewer_keywords: ["MI_Context_WriteVerbose","MI_Context_WriteVerbose function [Windows Management Infrastructure (MI)]","mi/MI_Context_WriteVerbose","wmi.mi_writeverbose","wmi_v2.mi_context_writeverbose"]
old-location: wmi_v2\mi_context_writeverbose.htm
tech.root: wmi_v2
ms.assetid: 55f46e42-3649-40f0-9bd6-4564afc2f8e2
ms.date: 12/05/2018
ms.keywords: MI_Context_WriteVerbose, MI_Context_WriteVerbose function [Windows Management Infrastructure (MI)], mi/MI_Context_WriteVerbose, wmi.mi_writeverbose, wmi_v2.mi_context_writeverbose
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
 - MI_Context_WriteVerbose
 - mi/MI_Context_WriteVerbose
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
 - MI_Context_WriteVerbose
---

# MI_Context_WriteVerbose function


## -description

Writes a verbose message to the client.

## -parameters

### -param context [in]

Request context.

### -param message

A null-terminated string that represents the message to be sent to the client. This string should be localized.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -remarks

A provider calls this function  when a verbose message needs to be sent to the client.  A verbose message indicates any progress a provider may be making or useful information that a client may need while running an operation.  A client can optionally register to receive these messages via an asynchronous callback.  If a client does not register for these messages, the server will ignore the message.