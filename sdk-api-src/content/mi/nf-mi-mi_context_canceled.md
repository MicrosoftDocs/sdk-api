---
UID: NF:mi.MI_Context_Canceled
title: MI_Context_Canceled function (mi.h)
description: Determines whether the operation has been canceled. This function is reserved; instead, use the MI_Context_RegisterCancel function.
helpviewer_keywords: ["MI_Context_Canceled","MI_Context_Canceled function [Windows Management Infrastructure (MI)]","mi/MI_Context_Canceled","wmi.mi_canceled","wmi_v2.mi_context_canceled"]
old-location: wmi_v2\mi_context_canceled.htm
tech.root: wmi_v2
ms.assetid: d8050079-978d-461b-8cf7-e6a08e4d026f
ms.date: 12/05/2018
ms.keywords: MI_Context_Canceled, MI_Context_Canceled function [Windows Management Infrastructure (MI)], mi/MI_Context_Canceled, wmi.mi_canceled, wmi_v2.mi_context_canceled
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
 - MI_Context_Canceled
 - mi/MI_Context_Canceled
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
 - MI_Context_Canceled
---

# MI_Context_Canceled function


## -description

Determines whether the operation has been canceled. This function is reserved; instead, use the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_registercancel">MI_Context_RegisterCancel</a> function.

## -parameters

### -param context [in]

A pointer to the request context that was passed to the provider method.

### -param flag [out]

A pointer to a flag that holds the deletion result. Upon return, this flag will be <b>MI_TRUE</b> if the operation has been successfully canceled; 
     otherwise, it will be <b>MI_FALSE</b>.

## -returns

This function returns MI_INLINE MI_Result MI_INLINE_CALL.

## -remarks

A canceled operation on the client does not always signal to the server that the operation should be canceled. It depends on both the type of operation and the support from the underlying protocol handler.