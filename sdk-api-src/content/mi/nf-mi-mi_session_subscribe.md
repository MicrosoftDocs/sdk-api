---
UID: NF:mi.MI_Session_Subscribe
title: MI_Session_Subscribe function (mi.h)
description: Subscribes to an indication on the server represented by the session.
helpviewer_keywords: ["MI_Session_Subscribe","MI_Session_Subscribe function [Windows Management Infrastructure (MI)]","mi/MI_Session_Subscribe","wmi_v2.mi_session_subscribe"]
old-location: wmi_v2\mi_session_subscribe.htm
tech.root: wmi_v2
ms.assetid: fed64a7a-ef16-4e9b-91b4-7ecede099585
ms.date: 12/05/2018
ms.keywords: MI_Session_Subscribe, MI_Session_Subscribe function [Windows Management Infrastructure (MI)], mi/MI_Session_Subscribe, wmi_v2.mi_session_subscribe
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
 - MI_Session_Subscribe
 - mi/MI_Session_Subscribe
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
 - MI_Session_Subscribe
---

# MI_Session_Subscribe function


## -description

Subscribes to an indication on the server represented by the session.

## -parameters

### -param session [in]

Session handle returned from <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newsession">MI_Application_NewSession</a>.

### -param flags

Runtime type information (RTTI) <a href="/previous-versions/windows/desktop/wmi_v2/mi-flags">flags</a>.

### -param options [in, optional]

Optional <a href="/windows/desktop/api/mi/ns-mi-mi_operationoptions">MI_OperationOptions</a> value that specifies options such as timeouts and how to control the CIM semantics. Specify <b>Null</b> if no operation options are to be sent.

### -param namespaceName

An optional, null-terminated string that represents the namespace name to carry out the operation.  If none is specified, the server will pick a default.  The namespace cannot include a computer name.  It can only be in the form of a namespace name separated by a slash mark character (/). For example, the following would be a valid <b>namespaceName</b> value: <b>root/cimv2</b>.

### -param queryDialect

An optional, null-terminated string that represents the dialect of the query being passed. This value can be either WQL or CQL. Note that some servers do not support both dialects.

### -param queryExpression

An optional, null-terminated string that represents the query expression to be carried out.  Usually a query is needed, but if a WS-Management endpoint is being used, a resource URI can be passed. For WMI DCOM transport, this value must be specified.

### -param deliverOptions [in, optional]

Optional <a href="/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a> structure that defines the subscription delivery options. For WMI DCOM transport, this value can be <b>Null</b>. For WinRM, this specifies settings such as delivery mode and push delivery credentials.

### -param callbacks [in, optional]

Optional <a href="/windows/desktop/api/mi/ns-mi-mi_operationcallbacks">MI_OperationCallbacks</a> structure that defines the operational callbacks to receive the instance result and CIM semantics. To carry out the operation asynchronously, the structure's <b>indicationResult</b> callback member must be specified. If this member is not specified, the client must call the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_getindication">MI_Operation_GetIndication</a> function to retrieve the results.

### -param operation [out]

Returned operation handle that must be closed via <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_close">MI_Operation_Close</a> once complete.  Calling <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_cancel">MI_Operation_Cancel</a> before it is complete will cause the operation to shutdown.  <b>MI_Operation_Close</b> and <b>MI_Operation_Cancel</b> can be called from any operation.

## -remarks

You must have Audit privileges to use this function if specifying the push subscriptions option.

## -see-also

<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newsession">MI_Application_NewSession</a>



<a href="/windows/desktop/api/mi/ns-mi-mi_operationcallbacks">MI_OperationCallbacks</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_cancel">MI_Operation_Cancel</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_close">MI_Operation_Close</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_getindication">MI_Operation_GetIndication</a>



<a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>