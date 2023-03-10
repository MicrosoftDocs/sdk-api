---
UID: NF:mi.MI_Session_Invoke
title: MI_Session_Invoke function (mi.h)
description: Invokes a method in the provider.
helpviewer_keywords: ["MI_Session_Invoke","MI_Session_Invoke function [Windows Management Infrastructure (MI)]","mi/MI_Session_Invoke","wmi_v2.mi_session_invoke"]
old-location: wmi_v2\mi_session_invoke.htm
tech.root: wmi_v2
ms.assetid: 46bce0cc-9795-47af-8318-4250dc3d5c6e
ms.date: 12/05/2018
ms.keywords: MI_Session_Invoke, MI_Session_Invoke function [Windows Management Infrastructure (MI)], mi/MI_Session_Invoke, wmi_v2.mi_session_invoke
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
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1,     Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - MI_Session_Invoke
 - mi/MI_Session_Invoke
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
 - MI_Session_Invoke
---

# MI_Session_Invoke function


## -description

Invokes a method in the provider.

## -parameters

### -param session [in]

Session handle returned from 
    <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newsession">MI_Application_NewSession</a>.

### -param flags

Runtime type information (RTTI) 
      <a href="/previous-versions/windows/desktop/wmi_v2/mi-flags">flags</a>.

### -param options [in, optional]

Optional <a href="/windows/desktop/api/mi/ns-mi-mi_operationoptions">MI_OperationOptions</a> value that 
      specifies options such as timeouts and how to control the CIM semantics. Specify <b>Null</b> 
      if no operation options are to be sent.

### -param namespaceName [in, optional]

An optional, null-terminated string that represents the namespace name to carry out the operation. If none 
      is specified, the server will pick a default.  The namespace cannot include a computer name.  It can only be in 
      the form of a namespace name separated by a slash mark character (/). For example, the following would be a 
      valid <b>namespaceName</b> value: <b>root/cimv2</b>.

### -param className [in, optional]

An optional, null-terminated string that represents the name of the class the method is a part of. Should 
      be <b>Null</b> when passing in an <b>inboundinstance</b>.

### -param methodName [in]

A null-terminated string that represents the name of the method to invoke.

### -param inboundInstance [in, optional]

Instance with keys to specify which method is to be invoked. If <b>Null</b>, the method 
      must be static.

### -param inboundProperties [in, optional]

Inbound method properties. Each inbound property needs to be an element in the instance and the element 
      name needs to be the same as the name of the method parameter.

### -param callbacks [in, optional]

Optional <a href="/windows/desktop/api/mi/ns-mi-mi_operationcallbacks">MI_OperationCallbacks</a> structure 
      that defines the operational callbacks to receive the instance result and CIM semantics. To carry out the 
      operation asynchronously, the structure's <b>instanceResult</b> callback member must be 
      specified. If this member is not specified, then the client must call the 
      <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_getinstance">MI_Operation_GetInstance</a> function to 
      retrieve the results.

### -param operation [out]

Returned operation handle that must be closed via 
      <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_close">MI_Operation_Close</a> once complete.  Calling 
      <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_cancel">MI_Operation_Cancel</a> before it is complete 
      will cause the operation to shutdown. 
      <b>MI_Operation_Close</b> and 
      <b>MI_Operation_Cancel</b> can be called from any 
      operation.

## -remarks

Methods have return values that will be returned as a <i>ReturnValue</i> parameter of the 
    outbound instance. There may be outbound properties that will be part of the same result. If the streamed 
    parameter callback is given and any outbound properties are marked as streamed, the streaming callback will be 
    called for each parameter that supports streaming. They will be called until all results are retrieved or until 
    the final result is given back.

## -see-also

<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newsession">MI_Application_NewSession</a>



<a href="/windows/desktop/api/mi/ns-mi-mi_operationcallbacks">MI_OperationCallbacks</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_cancel">MI_Operation_Cancel</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_close">MI_Operation_Close</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_getinstance">MI_Operation_GetInstance</a>