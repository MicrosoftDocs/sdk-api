---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

