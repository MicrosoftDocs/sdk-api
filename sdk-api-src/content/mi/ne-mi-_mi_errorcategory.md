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

# _MI_ErrorCategory enumeration


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



