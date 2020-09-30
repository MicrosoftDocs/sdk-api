---
UID: NF:mi.MI_Operation_Cancel
title: MI_Operation_Cancel function (mi.h)
description: Cancels a running operation.
helpviewer_keywords: ["MI_Operation_Cancel","MI_Operation_Cancel function [Windows Management Infrastructure (MI)]","mi/MI_Operation_Cancel","wmi_v2.mi_operation_cancel"]
old-location: wmi_v2\mi_operation_cancel.htm
tech.root: wmi_v2
ms.assetid: 11a9f9f6-9dfa-4f7c-9562-f4793c007f04
ms.date: 12/05/2018
ms.keywords: MI_Operation_Cancel, MI_Operation_Cancel function [Windows Management Infrastructure (MI)], mi/MI_Operation_Cancel, wmi_v2.mi_operation_cancel
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
 - MI_Operation_Cancel
 - mi/MI_Operation_Cancel
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
 - MI_Operation_Cancel
---

# MI_Operation_Cancel function


## -description

Cancels a running operation.

## -parameters

### -param operation [in, out]

A pointer to an operation handle that was returned from a call to one of the <a href="/windows/desktop/api/mi/ns-mi-mi_session">MI_Session</a> operation functions.  For asynchronous callbacks, this value can be the operation handle that is passed into the callback.

### -param reason

<a href="/windows/desktop/api/mi/ne-mi-mi_cancellationreason">MI_CancellationReason</a> enumeration value.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -remarks

Cancellation is asynchronous.  Cancelled operations still need to be closed.  Cancellation will cause the operation to finish as soon as possible. For an asynchronous operation, this will cause final callback to happen with the final result. For a synchronous operation, the final result should be available soon.

A closing operation, such as <b>MI_Operations_Cancel</b>, should be called in same security context as the starting operation.

After cancellation, there may be more than just one result, because cancellation happens as soon as possible, so a few extra results may still get delivered.  Not all operation cancellations get through to the provider for notification, though. (For example, enum can, but invoke cannot.)  The client does disconnect from the server as soon as possible, though, so it will not wait for the entire operation to complete before giving a final result.  Because not all operation cancellation can get to the server, it means that if the operation is taking quota (in terms of running operations, memory usage, and so on), then new operations may possibly fail with quota violations until the provider finally realizes the operation is canceled, and it shuts itself down.