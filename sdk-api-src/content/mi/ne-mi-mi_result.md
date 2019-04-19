---
UID: NE:mi._MI_Result
title: MI_Result (mi.h)
author: windows-sdk-content
description: Defines function return codes.
old-location: wmi_v2\mi_result.htm
tech.root: wmi_v2
ms.assetid: 9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MI_RESULT_ACCESS_DENIED, MI_RESULT_ALREADY_EXISTS, MI_RESULT_CLASS_HAS_CHILDREN, MI_RESULT_CLASS_HAS_INSTANCES, MI_RESULT_CONTINUATION_ON_ERROR_NOT_SUPPORTED, MI_RESULT_FAILED, MI_RESULT_FILTERED_ENUMERATION_NOT_SUPPORTED, MI_RESULT_INVALID_CLASS, MI_RESULT_INVALID_ENUMERATION_CONTEXT, MI_RESULT_INVALID_NAMESPACE, MI_RESULT_INVALID_OPERATION_TIMEOUT, MI_RESULT_INVALID_PARAMETER, MI_RESULT_INVALID_QUERY, MI_RESULT_INVALID_SUPERCLASS, MI_RESULT_METHOD_NOT_AVAILABLE, MI_RESULT_METHOD_NOT_FOUND, MI_RESULT_NAMESPACE_NOT_EMPTY, MI_RESULT_NOT_FOUND, MI_RESULT_NOT_SUPPORTED, MI_RESULT_NO_SUCH_PROPERTY, MI_RESULT_OK, MI_RESULT_PULL_CANNOT_BE_ABANDONED, MI_RESULT_PULL_HAS_BEEN_ABANDONED, MI_RESULT_QUERY_LANGUAGE_NOT_SUPPORTED, MI_RESULT_SERVER_IS_SHUTTING_DOWN, MI_RESULT_SERVER_LIMITS_EXCEEDED, MI_RESULT_TYPE_MISMATCH, MI_Result, MI_Result enumeration [Windows Management Infrastructure (MI)], _MI_Result, _MI_Result enumeration [Windows Management Infrastructure (MI)], mi/MI_RESULT_ACCESS_DENIED, mi/MI_RESULT_ALREADY_EXISTS, mi/MI_RESULT_CLASS_HAS_CHILDREN, mi/MI_RESULT_CLASS_HAS_INSTANCES, mi/MI_RESULT_CONTINUATION_ON_ERROR_NOT_SUPPORTED, mi/MI_RESULT_FAILED, mi/MI_RESULT_FILTERED_ENUMERATION_NOT_SUPPORTED, mi/MI_RESULT_INVALID_CLASS, mi/MI_RESULT_INVALID_ENUMERATION_CONTEXT, mi/MI_RESULT_INVALID_NAMESPACE, mi/MI_RESULT_INVALID_OPERATION_TIMEOUT, mi/MI_RESULT_INVALID_PARAMETER, mi/MI_RESULT_INVALID_QUERY, mi/MI_RESULT_INVALID_SUPERCLASS, mi/MI_RESULT_METHOD_NOT_AVAILABLE, mi/MI_RESULT_METHOD_NOT_FOUND, mi/MI_RESULT_NAMESPACE_NOT_EMPTY, mi/MI_RESULT_NOT_FOUND, mi/MI_RESULT_NOT_SUPPORTED, mi/MI_RESULT_NO_SUCH_PROPERTY, mi/MI_RESULT_OK, mi/MI_RESULT_PULL_CANNOT_BE_ABANDONED, mi/MI_RESULT_PULL_HAS_BEEN_ABANDONED, mi/MI_RESULT_QUERY_LANGUAGE_NOT_SUPPORTED, mi/MI_RESULT_SERVER_IS_SHUTTING_DOWN, mi/MI_RESULT_SERVER_LIMITS_EXCEEDED, mi/MI_RESULT_TYPE_MISMATCH, mi/MI_Result, wmi._mi_result, wmi_v2.mi_result
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - _MI_Result
product: Windows
targetos: Windows
req.typenames: MI_Result
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
---

# MI_Result enumeration


## -description


Defines function return codes.


## -enum-fields




### -field MI_RESULT_OK

The operation was successful.


### -field MI_RESULT_FAILED

A general error occurred, not covered by a more specific error code.


### -field MI_RESULT_ACCESS_DENIED

Access to a CIM resource is not available to the client. Reasons for this might be not having enough permissions to access the requested resources while carrying out the operation, 
or calling APIs with inconsistent identities. An example of the latter would be creating an <a href="https://msdn.microsoft.com/68a69321-0aa9-423e-a72f-aa2f4dee2d51">MI_Session</a> with one identity while trying to carry out an operation on the same session with a different identity.


### -field MI_RESULT_INVALID_NAMESPACE

The target namespace does not exist.


### -field MI_RESULT_INVALID_PARAMETER

One or more parameter values passed to the method are not valid.


### -field MI_RESULT_INVALID_CLASS

The specified class does not exist.


### -field MI_RESULT_NOT_FOUND

The requested object cannot be found.


### -field MI_RESULT_NOT_SUPPORTED

The requested operation is not supported.


### -field MI_RESULT_CLASS_HAS_CHILDREN

The operation cannot be invoked because the class has subclasses.


### -field MI_RESULT_CLASS_HAS_INSTANCES

The operation cannot be invoked because the class has instances.


### -field MI_RESULT_INVALID_SUPERCLASS

The operation cannot be invoked because the superclass does not exist.


### -field MI_RESULT_ALREADY_EXISTS

The operation cannot be invoked because an object already exists.


### -field MI_RESULT_NO_SUCH_PROPERTY

The specified property does not exist.


### -field MI_RESULT_TYPE_MISMATCH

The value supplied is not compatible with the type.


### -field MI_RESULT_QUERY_LANGUAGE_NOT_SUPPORTED

The query language is not recognized or supported.


### -field MI_RESULT_INVALID_QUERY

The query is not valid for the specified query language.


### -field MI_RESULT_METHOD_NOT_AVAILABLE

The extrinsic method cannot be invoked.


### -field MI_RESULT_METHOD_NOT_FOUND

The specified extrinsic method does not exist.


### -field MI_RESULT_NAMESPACE_NOT_EMPTY

The specified namespace is not empty.


### -field MI_RESULT_INVALID_ENUMERATION_CONTEXT

The enumeration identified by the specified context is not valid.


### -field MI_RESULT_INVALID_OPERATION_TIMEOUT

The specified operation time-out is not supported by the CIM Server.


### -field MI_RESULT_PULL_HAS_BEEN_ABANDONED

The pull operation has been abandoned.


### -field MI_RESULT_PULL_CANNOT_BE_ABANDONED

The attempt to abandon a concurrent pull operation failed.


### -field MI_RESULT_FILTERED_ENUMERATION_NOT_SUPPORTED

Using a filter in the enumeration is not supported by the CIM server.


### -field MI_RESULT_CONTINUATION_ON_ERROR_NOT_SUPPORTED

The CIM server does not support continuation on error.


### -field MI_RESULT_SERVER_LIMITS_EXCEEDED

The operation failed because server limits were exceeded.


### -field MI_RESULT_SERVER_IS_SHUTTING_DOWN

The CIM server is shutting down and cannot process the operation.

