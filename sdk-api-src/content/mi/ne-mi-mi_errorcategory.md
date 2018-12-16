---
UID: NE:mi._MI_ErrorCategory
title: MI_ErrorCategory
author: windows-sdk-content
description: This enumeration defines error categories for the CIM extensions.
old-location: wmi_v2\mi_errorcategory.htm
tech.root: wmi_v2
ms.assetid: afcc85a1-5aaf-41df-8cd7-b88739b73cf9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MI_ERRORCATEGORY_ACCESS_DENIED, MI_ERRORCATEGORY_CLOS_EERROR, MI_ERRORCATEGORY_DEADLOCK_DETECTED, MI_ERRORCATEGORY_DEVICE_ERROR, MI_ERRORCATEGORY_INVALID_ARGUMENT, MI_ERRORCATEGORY_INVALID_DATA, MI_ERRORCATEGORY_INVALID_OPERATION, MI_ERRORCATEGORY_INVALID_RESULT, MI_ERRORCATEGORY_INVALID_TYPE, MI_ERRORCATEGORY_METADATA_ERROR, MI_ERRORCATEGORY_NOT_IMPLEMENTED, MI_ERRORCATEGORY_NOT_INSTALLED, MI_ERRORCATEGORY_NOT_SPECIFIED, MI_ERRORCATEGORY_OBJECT_NOT_FOUND, MI_ERRORCATEGORY_OPEN_ERROR, MI_ERRORCATEGORY_OPERATION_STOPPED, MI_ERRORCATEGORY_OPERATION_TIMEOUT, MI_ERRORCATEGORY_PARSER_ERROR, MI_ERRORCATEGORY_READ_ERROR, MI_ERRORCATEGORY_RESOURCE_BUSY, MI_ERRORCATEGORY_RESOURCE_EXISTS, MI_ERRORCATEGORY_RESOURCE_UNAVAILABLE, MI_ERRORCATEGORY_SECURITY_ERROR, MI_ERRORCATEGORY_SYNTAX_ERROR, MI_ErrorCategory, MI_ErrorCategory enumeration [Windows Management Infrastructure (MI)], mi/MI_ERRORCATEGORY_ACCESS_DENIED, mi/MI_ERRORCATEGORY_CLOS_EERROR, mi/MI_ERRORCATEGORY_DEADLOCK_DETECTED, mi/MI_ERRORCATEGORY_DEVICE_ERROR, mi/MI_ERRORCATEGORY_INVALID_ARGUMENT, mi/MI_ERRORCATEGORY_INVALID_DATA, mi/MI_ERRORCATEGORY_INVALID_OPERATION, mi/MI_ERRORCATEGORY_INVALID_RESULT, mi/MI_ERRORCATEGORY_INVALID_TYPE, mi/MI_ERRORCATEGORY_METADATA_ERROR, mi/MI_ERRORCATEGORY_NOT_IMPLEMENTED, mi/MI_ERRORCATEGORY_NOT_INSTALLED, mi/MI_ERRORCATEGORY_NOT_SPECIFIED, mi/MI_ERRORCATEGORY_OBJECT_NOT_FOUND, mi/MI_ERRORCATEGORY_OPEN_ERROR, mi/MI_ERRORCATEGORY_OPERATION_STOPPED, mi/MI_ERRORCATEGORY_OPERATION_TIMEOUT, mi/MI_ERRORCATEGORY_PARSER_ERROR, mi/MI_ERRORCATEGORY_READ_ERROR, mi/MI_ERRORCATEGORY_RESOURCE_BUSY, mi/MI_ERRORCATEGORY_RESOURCE_EXISTS, mi/MI_ERRORCATEGORY_RESOURCE_UNAVAILABLE, mi/MI_ERRORCATEGORY_SECURITY_ERROR, mi/MI_ERRORCATEGORY_SYNTAX_ERROR, mi/MI_ErrorCategory, wmi._mi_errorcategory, wmi_v2.mi_errorcategory
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
 - MI_ErrorCategory
product: Windows
targetos: Windows
req.typenames: MI_ErrorCategory
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_ErrorCategory enumeration


## -description


This enumeration defines error categories for the CIM extensions.


## -enum-fields




### -field MI_ERRORCATEGORY_NOT_SPECIFIED

Use only when not enough is known about the error to assign it to another error category. Avoid using this category if you have any information about the error, even if that information is incomplete.


### -field MI_ERRORCATEGORY_OPEN_ERROR

An error that occurs when opening.


### -field MI_ERRORCATEGORY_CLOS_EERROR

An error that occurs when closing.


### -field MI_ERRORCATEGORY_DEVICE_ERROR

An error that occurs when a device reports an error.


### -field MI_ERRORCATEGORY_DEADLOCK_DETECTED

An error that occurs when a deadlock is detected.


### -field MI_ERRORCATEGORY_INVALID_ARGUMENT

An error that occurs when an argument that is not valid is specified.


### -field MI_ERRORCATEGORY_INVALID_DATA

An error that occurs when data that is not valid is specified.


### -field MI_ERRORCATEGORY_INVALID_OPERATION

An error that occurs when an operation that is not valid is requested.


### -field MI_ERRORCATEGORY_INVALID_RESULT

An error that occurs when a result that is not valid is returned.


### -field MI_ERRORCATEGORY_INVALID_TYPE

An error that occurs when a .NET Framework type that is not valid is specified.


### -field MI_ERRORCATEGORY_METADATA_ERROR

An error that occurs when metadata contains an error.


### -field MI_ERRORCATEGORY_NOT_IMPLEMENTED

An error that occurs when a referenced application programming interface (API) is not implemented.


### -field MI_ERRORCATEGORY_NOT_INSTALLED

An error that occurs when an item is not installed.


### -field MI_ERRORCATEGORY_OBJECT_NOT_FOUND

An error that occurs when an object cannot be found.


### -field MI_ERRORCATEGORY_OPERATION_STOPPED

An error that occurs when an operation has stopped. For example, the user interrupts the operation.


### -field MI_ERRORCATEGORY_OPERATION_TIMEOUT

An error that occurs when an operation has exceeded its timeout limit.


### -field MI_ERRORCATEGORY_SYNTAX_ERROR

An error that occurs when a command is syntactically incorrect.


### -field MI_ERRORCATEGORY_PARSER_ERROR

An error that occurs when a parser encounters an error.


### -field MI_ERRORCATEGORY_ACCESS_DENIED

An error that occurs when an operation is not permitted.


### -field MI_ERRORCATEGORY_RESOURCE_BUSY

An error that occurs when a resource already exists.


### -field MI_ERRORCATEGORY_RESOURCE_EXISTS

An error that occurs when a resource is busy.


### -field MI_ERRORCATEGORY_RESOURCE_UNAVAILABLE

An error that occurs when a resource is unavailable.


### -field MI_ERRORCATEGORY_READ_ERROR

An error that occurs when reading.


### -field MI_ERRORCATEGORY_WRITE_ERROR


### -field MI_ERRORCATEGORY_FROM_STDERR


### -field MI_ERRORCATEGORY_SECURITY_ERROR

An error that occurs when a security violation occurs.


### -field MI_ERRORCATEGORY_PROTOCOL_ERROR


### -field MI_ERRORCATEGORY_CONNECTION_ERROR


### -field MI_ERRORCATEGORY_AUTHENTICATION_ERROR


### -field MI_ERRORCATEGORY_LIMITS_EXCEEDED


### -field MI_ERRORCATEGORY_QUOTA_EXCEEDED


### -field MI_ERRORCATEGORY_NOT_ENABLED



