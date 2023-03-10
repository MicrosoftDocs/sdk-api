---
UID: NE:mi._MI_OperationCallback_ResponseType
title: MI_OperationCallback_ResponseType (mi.h)
description: If the MI_CallbackMode is MI_CALLBACKMODE_INQUIRE, one of these values can be used in the callback.
helpviewer_keywords: ["MI_OperationCallback_ResponseType","MI_OperationCallback_ResponseType enumeration [Windows Management Infrastructure (MI)]","MI_OperationCallback_ResponseType_No","MI_OperationCallback_ResponseType_NoToAll","MI_OperationCallback_ResponseType_Yes","MI_OperationCallback_ResponseType_YesToAll","mi/MI_OperationCallback_ResponseType","mi/MI_OperationCallback_ResponseType_No","mi/MI_OperationCallback_ResponseType_NoToAll","mi/MI_OperationCallback_ResponseType_Yes","mi/MI_OperationCallback_ResponseType_YesToAll","wmi._mi_operationcallback_responsetype","wmi_v2.mi_operationcallback_responsetype"]
old-location: wmi_v2\mi_operationcallback_responsetype.htm
tech.root: wmi_v2
ms.assetid: 07e1d42b-b9e4-4199-88b1-71864de37282
ms.date: 12/05/2018
ms.keywords: MI_OperationCallback_ResponseType, MI_OperationCallback_ResponseType enumeration [Windows Management Infrastructure (MI)], MI_OperationCallback_ResponseType_No, MI_OperationCallback_ResponseType_NoToAll, MI_OperationCallback_ResponseType_Yes, MI_OperationCallback_ResponseType_YesToAll, mi/MI_OperationCallback_ResponseType, mi/MI_OperationCallback_ResponseType_No, mi/MI_OperationCallback_ResponseType_NoToAll, mi/MI_OperationCallback_ResponseType_Yes, mi/MI_OperationCallback_ResponseType_YesToAll, wmi._mi_operationcallback_responsetype, wmi_v2.mi_operationcallback_responsetype
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
req.typenames: MI_OperationCallback_ResponseType
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_OperationCallback_ResponseType
 - mi/_MI_OperationCallback_ResponseType
 - MI_OperationCallback_ResponseType
 - mi/MI_OperationCallback_ResponseType
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
 - MI_OperationCallback_ResponseType
---

# MI_OperationCallback_ResponseType enumeration


## -description

If the MI_CallbackMode is MI_CALLBACKMODE_INQUIRE, one of these values can be used in the callback.

## -enum-fields

### -field MI_OperationCallback_ResponseType_No

No to this request only.

### -field MI_OperationCallback_ResponseType_Yes

Yes to this request only.

### -field MI_OperationCallback_ResponseType_NoToAll

No to this request and all future requests from this operation.

### -field MI_OperationCallback_ResponseType_YesToAll

Yes to this request and all future requests from this operation.

