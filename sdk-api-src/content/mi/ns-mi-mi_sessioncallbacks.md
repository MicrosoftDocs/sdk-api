---
UID: NS:mi._MI_SessionCallbacks
title: MI_SessionCallbacks (mi.h)
description: A container for callback function pointers that handle logging and error messages.
helpviewer_keywords: ["MI_SessionCallbacks","MI_SessionCallbacks structure [Windows Management Infrastructure (MI)]","mi/MI_SessionCallbacks","wmi_v2.mi_sessioncallbacks"]
old-location: wmi_v2\mi_sessioncallbacks.htm
tech.root: wmi_v2
ms.assetid: 76b21381-201e-4128-b0db-18d8968a80bb
ms.date: 12/05/2018
ms.keywords: MI_SessionCallbacks, MI_SessionCallbacks structure [Windows Management Infrastructure (MI)], mi/MI_SessionCallbacks, wmi_v2.mi_sessioncallbacks
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
req.typenames: MI_SessionCallbacks
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_SessionCallbacks
 - mi/_MI_SessionCallbacks
 - MI_SessionCallbacks
 - mi/MI_SessionCallbacks
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
 - MI_SessionCallbacks
---

## -description

A container for callback function pointers that handle logging and error messages.

## -struct-fields

### -field callbackContext

A client-specific context that is passed to all of the callbacks. This is used to correlate the callback to the associated operation.

### -field writeError

The CIM extension callback for errors. The session version of this function is informative only. The session will fail to create and will  return an error. All parameters are valid only for the lifetime of the callback.

### -field writeMessage

The CIM extension callback for receiving logging from the session creation. All parameters are valid only for the lifetime of the callback.

## -remarks

This is the structure that holds all callback function pointers. Fill in the ones 
you want to receive. All callbacks are CIM extensions for tracking
logging and error messages.
