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

# _MI_Result enumeration


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

