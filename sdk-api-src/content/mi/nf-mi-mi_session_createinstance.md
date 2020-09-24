---
UID: NF:mi.MI_Session_CreateInstance
title: MI_Session_CreateInstance function (mi.h)
description: Creates an instance on the server that the session represents.
helpviewer_keywords: ["MI_Session_CreateInstance","MI_Session_CreateInstance function [Windows Management Infrastructure (MI)]","mi/MI_Session_CreateInstance","wmi_v2.mi_session_createinstance"]
old-location: wmi_v2\mi_session_createinstance.htm
tech.root: wmi_v2
ms.assetid: ad4df737-4438-4bcd-8b58-ae5c6b25e95f
ms.date: 12/05/2018
ms.keywords: MI_Session_CreateInstance, MI_Session_CreateInstance function [Windows Management Infrastructure (MI)], mi/MI_Session_CreateInstance, wmi_v2.mi_session_createinstance
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
 - MI_Session_CreateInstance
 - mi/MI_Session_CreateInstance
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
 - MI_Session_CreateInstance
---

# MI_Session_CreateInstance function


## -description

Creates an instance on the server that the session represents.

## -parameters

### -param session [in]

Session handle returned from <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newsession">MI_Application_NewSession</a>.

### -param flags

Runtime type information (RTTI) <a href="/previous-versions/windows/desktop/wmi_v2/mi-flags">flags</a>.

### -param options [in, optional]

Optional <a href="/windows/desktop/api/mi/ns-mi-mi_operationoptions">MI_OperationOptions</a> value that specifies options such as timeouts and how to control the CIM semantics. Specify <b>Null</b> if no operation options are to be sent.

### -param namespaceName

A null-terminated string that contains the optional namespace name to carry out the operation.  If none is specified, the server will pick a default.  The namespace cannot include a computer name.  It can only be in the form of a namespace name separated by a slash mark character (/). For example, the following would be a valid <b>namespaceName</b> value: <b>root/cimv2</b>.

### -param inboundInstance [in]

<a href="/windows/desktop/api/mi/ns-mi-mi_instance">MI_Instance</a> that represents the class name and keys of the instance to be created on the server along with the rest of the properties of the instance that destination instance will be set to.  Sometimes keys are read-only, so not all keys need to be specified. If the instance that is specified already exists, the function will fail; to update an existing instance, use the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_session_modifyinstance">MI_Session_ModifyInstance</a> function.

### -param callbacks [in, optional]

Optional <a href="/windows/desktop/api/mi/ns-mi-mi_operationcallbacks">MI_OperationCallbacks</a> structure that defines the operational callbacks to receive the instance result and CIM semantics. To do asynchronously, this value must be specified. If NULL is specified, the client must call the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_getinstance">MI_Operation_GetInstance</a> function to retrieve the results.

### -param operation [out]

Operation handle that must be closed with a call to <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_close">MI_Operation_Close</a> once the operation is finished and all results have been received. The handle can be used to cancel the operation with a call to <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_cancel">MI_Operation_Cancel</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_cancel">MI_Operation_Cancel</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_close">MI_Operation_Close</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_getinstance">MI_Operation_GetInstance</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_session_modifyinstance">MI_Session_ModifyInstance</a>