---
UID: NF:mi.MI_Session_DeleteInstance
title: MI_Session_DeleteInstance function (mi.h)
description: Deletes an instance on the server represented by the session.
helpviewer_keywords: ["MI_Session_DeleteInstance","MI_Session_DeleteInstance function [Windows Management Infrastructure (MI)]","mi/MI_Session_DeleteInstance","wmi_v2.mi_session_deleteinstance"]
old-location: wmi_v2\mi_session_deleteinstance.htm
tech.root: wmi_v2
ms.assetid: 10d49e33-adbc-4202-91f6-7df9b4cff133
ms.date: 12/05/2018
ms.keywords: MI_Session_DeleteInstance, MI_Session_DeleteInstance function [Windows Management Infrastructure (MI)], mi/MI_Session_DeleteInstance, wmi_v2.mi_session_deleteinstance
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
 - MI_Session_DeleteInstance
 - mi/MI_Session_DeleteInstance
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
 - MI_Session_DeleteInstance
---

# MI_Session_DeleteInstance function


## -description

Deletes an instance on the server represented by the session.

## -parameters

### -param session [in]

Session handle returned from <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newsession">MI_Application_NewSession</a>.

### -param flags

Must be 0.

### -param options [in, optional]

Optional <a href="/windows/desktop/api/mi/ns-mi-mi_operationoptions">MI_OperationOptions</a> value that specifies options such as timeouts and how to control the CIM semantics. Specify <b>NULL</b> if no operation options are to be sent.

### -param namespaceName

An optional, null-terminated string that represents the namespace name to carry out the operation.  If none is specified, the server will pick a default.  The namespace cannot include a computer name.  It can only be in the form of a namespace name separated by a slash mark character (/). For example, the following would be a valid <b>namespaceName</b> value: <b>root/cimv2</b>.

### -param inboundInstance [in]

<a href="/windows/desktop/api/mi/ns-mi-mi_instance">MI_Instance</a> that represents the class name and key of the instance to be deleted on the server.

### -param callbacks [in, optional]

Optional <a href="/windows/desktop/api/mi/ns-mi-mi_operationcallbacks">MI_OperationCallbacks</a> structure that defines the operational callbacks to receive the instance result and CIM semantics. A callback value is required to carry out the operation asynchronously. If <b>NULL</b> is specified, then the client must call the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_getinstance">MI_Operation_GetInstance</a> function to retrieve the results.

### -param operation [out]

Operation handle that must be closed with a call to <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_close">MI_Operation_Close</a> once the operation is finished and all results have been received. The handle can be used to cancel the operation with a call to <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_cancel">MI_Operation_Cancel</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newsession">MI_Application_NewSession</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_cancel">MI_Operation_Cancel</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_close">MI_Operation_Close</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_getinstance">MI_Operation_GetInstance</a>