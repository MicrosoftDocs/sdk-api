---
UID: NF:mi.MI_Session_AssociatorInstances
title: MI_Session_AssociatorInstances function (mi.h)
description: Finds instances that are associated with the specific key instance.
helpviewer_keywords: ["MI_Session_AssociatorInstances","MI_Session_AssociatorInstances function [Windows Management Infrastructure (MI)]","mi/MI_Session_AssociatorInstances","wmi_v2.mi_session_associatorinstances"]
old-location: wmi_v2\mi_session_associatorinstances.htm
tech.root: wmi_v2
ms.assetid: 4e517289-a30e-4ba3-8cbf-dfc4f9744b1a
ms.date: 12/05/2018
ms.keywords: MI_Session_AssociatorInstances, MI_Session_AssociatorInstances function [Windows Management Infrastructure (MI)], mi/MI_Session_AssociatorInstances, wmi_v2.mi_session_associatorinstances
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
 - MI_Session_AssociatorInstances
 - mi/MI_Session_AssociatorInstances
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
 - MI_Session_AssociatorInstances
---

# MI_Session_AssociatorInstances function


## -description

Finds instances that are associated with the specific key instance.

## -parameters

### -param session [in]

Handle created from a call to <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newsession">MI_Application_NewSession</a>.

### -param flags

Runtime type information (RTTI) <a href="/previous-versions/windows/desktop/wmi_v2/mi-flags">flags</a>.

### -param options [in, optional]

Optional <a href="/windows/desktop/api/mi/ns-mi-mi_operationoptions">MI_OperationOptions</a> value that specifies options such as timeouts and how to control the CIM semantics. Specify NULL if no operation options are to be sent.

### -param namespaceName

A null-terminated string that contains the optional namespace name to carry out the operation.  If none is specified the server will pick a default.  The namespace cannot include a computer name.  It can only be in the form of namespace names separated by a slash character, for instance root/cimv2.

### -param instanceKey [in]

An <a href="/windows/desktop/api/mi/ns-mi-mi_instance">MI_Instance</a> that represents the class name and the keys of the instance where the association will start.

### -param assocClass

A null-terminated string that represents the optional value that specifies to only map the association via this association class. If this value is NULL, then any association classes will be used.

### -param resultClass

A null-terminated string that represents the optional values that restricts the result set to only this class. Specify NULL if no filtering is wanted.

### -param role

A null-terminated string that represents the property name in the association object that points to our key object.

### -param resultRole

A null-terminated string that represents the property name in the association object that points to the resultant class.

### -param keysOnly

If set to MI_TRUE the operation will only retrieve the key properties of the instances. Otherwise, specify MI_FALSE.

### -param callbacks [in, optional]

Optional <a href="/windows/desktop/api/mi/ns-mi-mi_operationcallbacks">MI_OperationCallbacks</a> structure that defines the operational callbacks to receive the instance result and CIM semantics. For asynchronous operation, the callback must be specified. For synchronous operation, specify NULL; the client must then call <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_getinstance">MI_Operation_GetInstance</a> to retrieve the results.

### -param operation [out]

Operation handle that must be closed with a call to <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_close">MI_Operation_Close</a> once the operation is finished and all results have been received. The handle can be used to cancel the operation with a call to <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_cancel">MI_Operation_Cancel</a>.

## -remarks

An association is a relationship between two objects. It is represented with a third object containing two properties, each being a reference to one of those two related objects. The <i>role</i> parameter is the association object's reference property, pointing to the object being associated. The <i>resultRole</i> parameter points to the other, resultant object.

## -see-also

<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newsession">MI_Application_NewSession</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_cancel">MI_Operation_Cancel</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_close">MI_Operation_Close</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_getinstance">MI_Operation_GetInstance</a>