---
UID: NF:mi.MI_Operation_GetIndication
title: MI_Operation_GetIndication function (mi.h)
description: Get the synchronous results from a subscription.
helpviewer_keywords: ["MI_Operation_GetIndication","MI_Operation_GetIndication function [Windows Management Infrastructure (MI)]","mi/MI_Operation_GetIndication","wmi_v2.mi_operation_getindication"]
old-location: wmi_v2\mi_operation_getindication.htm
tech.root: wmi_v2
ms.assetid: 3e3e8472-ea33-485b-9e86-b5ba770af95b
ms.date: 12/05/2018
ms.keywords: MI_Operation_GetIndication, MI_Operation_GetIndication function [Windows Management Infrastructure (MI)], mi/MI_Operation_GetIndication, wmi_v2.mi_operation_getindication
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
 - MI_Operation_GetIndication
 - mi/MI_Operation_GetIndication
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
 - MI_Operation_GetIndication
---

# MI_Operation_GetIndication function


## -description

Get the synchronous results from a subscription.

## -parameters

### -param operation [in]

Operation handle returned from an instance session operation.

### -param instance

Returned indication instance. If the operation fails, this value may be <b>Null</b>. The returned class is valid until the next call to <b>MI_Operation_GetIndication</b> or <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_close">MI_Operation_Close</a>. If the class needs to be stay active across these calls, then the class needs to be cloned via <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_clone">MI_Instance_Clone</a>.

### -param bookmark

Some providers allow a subscription to resume from a particular indication result should the subscription fail or get shut down. If the provider supports this, then a bookmark is optionally returned with the instance. This bookmark can then be passed in to a future subscription to attempt to resume the subscription from that point. Most providers do not support this functionality.

### -param machineID

Returned machine identification indicating the origin of the event.

### -param moreResults [out, optional]

Returned Boolean value indicating if more results are available. A value of <b>MI_TRUE</b> means that more results can be retrieved. This function must be called until <b>moreResults</b> has a value of <b>MI_FALSE</b> (even if the operation is canceled via <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_cancel">MI_Operation_Cancel</a>). Calling <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_close">MI_Operation_Close</a> before retrieving the last result where <b>moreResults</b> is set to <b>MI_FALSE</b> will cause the <b>MI_Operation_Close</b> function to stop responding.

### -param result [out, optional]

Returned value indicating the success or failure of the function call. A value of <b>MI_RESULT_OK</b> indicates success. Otherwise, the returned <b>errorMessage</b> value should be used to determine the cause of failure.

### -param errorMessage

In the case of an error, this returned value provides additional debugging information as to the cause of failure. This error message has the same lifetime as the <b>classResult</b> value.

### -param completionDetails

In the case of an error, this returned value provides additional error information - typically in the form of a CIM_Error object (or a derived class). This returned instance has the same lifetime as the <b>classResult</b> value. If this value is needs to stay active longer, then the value needs to be cloned via <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_clone">MI_Instance_Clone</a>.

## -remarks

This function will block until a new indication arrives.  This function should not be called on non-subscription calls or a non-subscription operation.