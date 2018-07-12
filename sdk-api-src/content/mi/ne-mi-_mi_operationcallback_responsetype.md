---
UID: NE:mi._MI_OperationCallback_ResponseType
title: "_MI_OperationCallback_ResponseType"
author: windows-sdk-content
description: If the MI_CallbackMode is MI_CALLBACKMODE_INQUIRE, one of these values can be used in the callback.
old-location: wmi_v2\mi_operationcallback_responsetype.htm
old-project: wmi_v2
ms.assetid: 07e1d42b-b9e4-4199-88b1-71864de37282
ms.author: windowssdkdev
ms.date: 06/14/2018
ms.keywords: MI_OperationCallback_ResponseType, MI_OperationCallback_ResponseType enumeration [Windows Management Infrastructure (MI)], MI_OperationCallback_ResponseType_No, MI_OperationCallback_ResponseType_NoToAll, MI_OperationCallback_ResponseType_Yes, MI_OperationCallback_ResponseType_YesToAll, _MI_OperationCallback_ResponseType, mi/MI_OperationCallback_ResponseType, mi/MI_OperationCallback_ResponseType_No, mi/MI_OperationCallback_ResponseType_NoToAll, mi/MI_OperationCallback_ResponseType_Yes, mi/MI_OperationCallback_ResponseType_YesToAll, wmi._mi_operationcallback_responsetype, wmi_v2.mi_operationcallback_responsetype
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: MI_OperationCallback_ResponseType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_OperationCallback_ResponseType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MI_OperationCallback_ResponseType enumeration


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

