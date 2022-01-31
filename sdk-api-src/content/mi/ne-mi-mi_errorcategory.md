---
UID: NE:mi._MI_ErrorCategory
title: MI_ErrorCategory (mi.h)
description: This enumeration defines error categories for the CIM extensions.
helpviewer_keywords: ["MI_ERRORCATEGORY_ACCESS_DENIED","MI_ERRORCATEGORY_CLOS_EERROR","MI_ERRORCATEGORY_DEADLOCK_DETECTED","MI_ERRORCATEGORY_DEVICE_ERROR","MI_ERRORCATEGORY_INVALID_ARGUMENT","MI_ERRORCATEGORY_INVALID_DATA","MI_ERRORCATEGORY_INVALID_OPERATION","MI_ERRORCATEGORY_INVALID_RESULT","MI_ERRORCATEGORY_INVALID_TYPE","MI_ERRORCATEGORY_METADATA_ERROR","MI_ERRORCATEGORY_NOT_IMPLEMENTED","MI_ERRORCATEGORY_NOT_INSTALLED","MI_ERRORCATEGORY_NOT_SPECIFIED","MI_ERRORCATEGORY_OBJECT_NOT_FOUND","MI_ERRORCATEGORY_OPEN_ERROR","MI_ERRORCATEGORY_OPERATION_STOPPED","MI_ERRORCATEGORY_OPERATION_TIMEOUT","MI_ERRORCATEGORY_PARSER_ERROR","MI_ERRORCATEGORY_READ_ERROR","MI_ERRORCATEGORY_RESOURCE_BUSY","MI_ERRORCATEGORY_RESOURCE_EXISTS","MI_ERRORCATEGORY_RESOURCE_UNAVAILABLE","MI_ERRORCATEGORY_SECURITY_ERROR","MI_ERRORCATEGORY_SYNTAX_ERROR","MI_ErrorCategory","MI_ErrorCategory enumeration [Windows Management Infrastructure (MI)]","mi/MI_ERRORCATEGORY_ACCESS_DENIED","mi/MI_ERRORCATEGORY_CLOS_EERROR","mi/MI_ERRORCATEGORY_DEADLOCK_DETECTED","mi/MI_ERRORCATEGORY_DEVICE_ERROR","mi/MI_ERRORCATEGORY_INVALID_ARGUMENT","mi/MI_ERRORCATEGORY_INVALID_DATA","mi/MI_ERRORCATEGORY_INVALID_OPERATION","mi/MI_ERRORCATEGORY_INVALID_RESULT","mi/MI_ERRORCATEGORY_INVALID_TYPE","mi/MI_ERRORCATEGORY_METADATA_ERROR","mi/MI_ERRORCATEGORY_NOT_IMPLEMENTED","mi/MI_ERRORCATEGORY_NOT_INSTALLED","mi/MI_ERRORCATEGORY_NOT_SPECIFIED","mi/MI_ERRORCATEGORY_OBJECT_NOT_FOUND","mi/MI_ERRORCATEGORY_OPEN_ERROR","mi/MI_ERRORCATEGORY_OPERATION_STOPPED","mi/MI_ERRORCATEGORY_OPERATION_TIMEOUT","mi/MI_ERRORCATEGORY_PARSER_ERROR","mi/MI_ERRORCATEGORY_READ_ERROR","mi/MI_ERRORCATEGORY_RESOURCE_BUSY","mi/MI_ERRORCATEGORY_RESOURCE_EXISTS","mi/MI_ERRORCATEGORY_RESOURCE_UNAVAILABLE","mi/MI_ERRORCATEGORY_SECURITY_ERROR","mi/MI_ERRORCATEGORY_SYNTAX_ERROR","mi/MI_ErrorCategory","wmi._mi_errorcategory","wmi_v2.mi_errorcategory"]
old-location: wmi_v2\mi_errorcategory.htm
tech.root: wmi_v2
ms.assetid: afcc85a1-5aaf-41df-8cd7-b88739b73cf9
ms.date: 12/05/2018
ms.keywords: MI_ERRORCATEGORY_ACCESS_DENIED, MI_ERRORCATEGORY_CLOS_EERROR, MI_ERRORCATEGORY_DEADLOCK_DETECTED, MI_ERRORCATEGORY_DEVICE_ERROR, MI_ERRORCATEGORY_INVALID_ARGUMENT, MI_ERRORCATEGORY_INVALID_DATA, MI_ERRORCATEGORY_INVALID_OPERATION, MI_ERRORCATEGORY_INVALID_RESULT, MI_ERRORCATEGORY_INVALID_TYPE, MI_ERRORCATEGORY_METADATA_ERROR, MI_ERRORCATEGORY_NOT_IMPLEMENTED, MI_ERRORCATEGORY_NOT_INSTALLED, MI_ERRORCATEGORY_NOT_SPECIFIED, MI_ERRORCATEGORY_OBJECT_NOT_FOUND, MI_ERRORCATEGORY_OPEN_ERROR, MI_ERRORCATEGORY_OPERATION_STOPPED, MI_ERRORCATEGORY_OPERATION_TIMEOUT, MI_ERRORCATEGORY_PARSER_ERROR, MI_ERRORCATEGORY_READ_ERROR, MI_ERRORCATEGORY_RESOURCE_BUSY, MI_ERRORCATEGORY_RESOURCE_EXISTS, MI_ERRORCATEGORY_RESOURCE_UNAVAILABLE, MI_ERRORCATEGORY_SECURITY_ERROR, MI_ERRORCATEGORY_SYNTAX_ERROR, MI_ErrorCategory, MI_ErrorCategory enumeration [Windows Management Infrastructure (MI)], mi/MI_ERRORCATEGORY_ACCESS_DENIED, mi/MI_ERRORCATEGORY_CLOS_EERROR, mi/MI_ERRORCATEGORY_DEADLOCK_DETECTED, mi/MI_ERRORCATEGORY_DEVICE_ERROR, mi/MI_ERRORCATEGORY_INVALID_ARGUMENT, mi/MI_ERRORCATEGORY_INVALID_DATA, mi/MI_ERRORCATEGORY_INVALID_OPERATION, mi/MI_ERRORCATEGORY_INVALID_RESULT, mi/MI_ERRORCATEGORY_INVALID_TYPE, mi/MI_ERRORCATEGORY_METADATA_ERROR, mi/MI_ERRORCATEGORY_NOT_IMPLEMENTED, mi/MI_ERRORCATEGORY_NOT_INSTALLED, mi/MI_ERRORCATEGORY_NOT_SPECIFIED, mi/MI_ERRORCATEGORY_OBJECT_NOT_FOUND, mi/MI_ERRORCATEGORY_OPEN_ERROR, mi/MI_ERRORCATEGORY_OPERATION_STOPPED, mi/MI_ERRORCATEGORY_OPERATION_TIMEOUT, mi/MI_ERRORCATEGORY_PARSER_ERROR, mi/MI_ERRORCATEGORY_READ_ERROR, mi/MI_ERRORCATEGORY_RESOURCE_BUSY, mi/MI_ERRORCATEGORY_RESOURCE_EXISTS, mi/MI_ERRORCATEGORY_RESOURCE_UNAVAILABLE, mi/MI_ERRORCATEGORY_SECURITY_ERROR, mi/MI_ERRORCATEGORY_SYNTAX_ERROR, mi/MI_ErrorCategory, wmi._mi_errorcategory, wmi_v2.mi_errorcategory
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
req.typenames: MI_ErrorCategory
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_ErrorCategory
 - mi/_MI_ErrorCategory
 - MI_ErrorCategory
 - mi/MI_ErrorCategory
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
 - MI_ErrorCategory
---

# MI_ErrorCategory enumeration


## -description

This enumeration defines error categories for the CIM extensions.

## -enum-fields

### -field MI_ERRORCATEGORY_NOT_SPECIFIED:0

Use only when not enough is known about the error to assign it to another error category. Avoid using this category if you have any information about the error, even if that information is incomplete.

### -field MI_ERRORCATEGORY_OPEN_ERROR:1

An error that occurs when opening.

### -field MI_ERRORCATEGORY_CLOS_EERROR:2

An error that occurs when closing.

### -field MI_ERRORCATEGORY_DEVICE_ERROR:3

An error that occurs when a device reports an error.

### -field MI_ERRORCATEGORY_DEADLOCK_DETECTED:4

An error that occurs when a deadlock is detected.

### -field MI_ERRORCATEGORY_INVALID_ARGUMENT:5

An error that occurs when an argument that is not valid is specified.

### -field MI_ERRORCATEGORY_INVALID_DATA:6

An error that occurs when data that is not valid is specified.

### -field MI_ERRORCATEGORY_INVALID_OPERATION:7

An error that occurs when an operation that is not valid is requested.

### -field MI_ERRORCATEGORY_INVALID_RESULT:8

An error that occurs when a result that is not valid is returned.

### -field MI_ERRORCATEGORY_INVALID_TYPE:9

An error that occurs when a .NET Framework type that is not valid is specified.

### -field MI_ERRORCATEGORY_METADATA_ERROR:10

An error that occurs when metadata contains an error.

### -field MI_ERRORCATEGORY_NOT_IMPLEMENTED:11

An error that occurs when a referenced application programming interface (API) is not implemented.

### -field MI_ERRORCATEGORY_NOT_INSTALLED:12

An error that occurs when an item is not installed.

### -field MI_ERRORCATEGORY_OBJECT_NOT_FOUND:13

An error that occurs when an object cannot be found.

### -field MI_ERRORCATEGORY_OPERATION_STOPPED:14

An error that occurs when an operation has stopped. For example, the user interrupts the operation.

### -field MI_ERRORCATEGORY_OPERATION_TIMEOUT:15

An error that occurs when an operation has exceeded its timeout limit.

### -field MI_ERRORCATEGORY_SYNTAX_ERROR:16

An error that occurs when a command is syntactically incorrect.

### -field MI_ERRORCATEGORY_PARSER_ERROR:17

An error that occurs when a parser encounters an error.

### -field MI_ERRORCATEGORY_ACCESS_DENIED:18

An error that occurs when an operation is not permitted.

### -field MI_ERRORCATEGORY_RESOURCE_BUSY:19

An error that occurs when a resource already exists.

### -field MI_ERRORCATEGORY_RESOURCE_EXISTS:20

An error that occurs when a resource is busy.

### -field MI_ERRORCATEGORY_RESOURCE_UNAVAILABLE:21

An error that occurs when a resource is unavailable.

### -field MI_ERRORCATEGORY_READ_ERROR:22

An error that occurs when reading.

### -field MI_ERRORCATEGORY_WRITE_ERROR:23

### -field MI_ERRORCATEGORY_FROM_STDERR:24

### -field MI_ERRORCATEGORY_SECURITY_ERROR:25

An error that occurs when a security violation occurs.

### -field MI_ERRORCATEGORY_PROTOCOL_ERROR:26

### -field MI_ERRORCATEGORY_CONNECTION_ERROR:27

### -field MI_ERRORCATEGORY_AUTHENTICATION_ERROR:28

### -field MI_ERRORCATEGORY_LIMITS_EXCEEDED:29

### -field MI_ERRORCATEGORY_QUOTA_EXCEEDED:30

### -field MI_ERRORCATEGORY_NOT_ENABLED:31

