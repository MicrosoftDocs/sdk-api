---
UID: NE:webservices.WS_FAULT_ERROR_PROPERTY_ID
title: WS_FAULT_ERROR_PROPERTY_ID
author: windows-sdk-content
description: Information about a fault.
old-location: wsw\ws_fault_error_property_id.htm
tech.root: wsw
ms.assetid: f5ae9ee9-18de-428d-9367-aa4a554577ea
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: WS_FAULT_ERROR_PROPERTY_ACTION, WS_FAULT_ERROR_PROPERTY_FAULT, WS_FAULT_ERROR_PROPERTY_HEADER, WS_FAULT_ERROR_PROPERTY_ID, WS_FAULT_ERROR_PROPERTY_ID enumeration [Web Services for Windows], webservices/WS_FAULT_ERROR_PROPERTY_ACTION, webservices/WS_FAULT_ERROR_PROPERTY_FAULT, webservices/WS_FAULT_ERROR_PROPERTY_HEADER, webservices/WS_FAULT_ERROR_PROPERTY_ID, wsw.ws_fault_error_property_id
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - WebServices.h
api_name:
 - WS_FAULT_ERROR_PROPERTY_ID
product: Windows
targetos: Windows
req.typenames: WS_FAULT_ERROR_PROPERTY_ID
req.redist: 
---

# WS_FAULT_ERROR_PROPERTY_ID enumeration


## -description


Information about a fault.


## -enum-fields




### -field WS_FAULT_ERROR_PROPERTY_FAULT

An optional <a href="https://msdn.microsoft.com/7fe0b142-04a1-4a92-99ca-523412f7c94e">WS_FAULT</a> value that is the fault representation of the error.  If no
                    fault representation is present, then the value is <b>NULL</b>.
                

To set the WS_FAULT value, pass a WS_FAULT* to <a href="https://msdn.microsoft.com/193664ab-4688-49c9-97e7-ccf2b3e2d7e8">WsSetFaultErrorProperty</a>.
                    The error object will make a copy of the WS_FAULT.  The error object will also
                    add the fault string of the fault to the set of error strings in the error object
                    if the language of the fault string matches that of the error object.
                

To get the WS_FAULT value, pass a WS_FAULT** to <a href="https://msdn.microsoft.com/b59e6ac6-a3f1-4a72-a941-f588950ba85a">WsGetFaultErrorProperty</a>, 
                    which will either return <b>NULL</b> (indicating no fault has been set), or will 
                    return a non-<b>NULL</b> pointer to the WS_FAULT.  The non-<b>NULL</b> pointer is valid until
                    <a href="https://msdn.microsoft.com/a01a65f1-3eca-452c-a10d-dc9c6c3db124">WsResetError</a> or <a href="https://msdn.microsoft.com/61da7bc2-b805-4379-a6b2-1e92374be1a0">WsFreeError</a> are called for the error object.
                

The default value is <b>NULL</b>.
                


### -field WS_FAULT_ERROR_PROPERTY_ACTION

An optional <a href="https://msdn.microsoft.com/3daa656f-7f97-4e29-a556-7ff72206f01c">WS_XML_STRING</a> value representing the action to use for the fault.
                    If the length of the string is zero, then no action is present.
                

To get the string value, pass a WS_XML_STRING* to <a href="https://msdn.microsoft.com/b59e6ac6-a3f1-4a72-a941-f588950ba85a">WsGetFaultErrorProperty</a>.
                    The returned string is valid until <a href="https://msdn.microsoft.com/a01a65f1-3eca-452c-a10d-dc9c6c3db124">WsResetError</a> or <a href="https://msdn.microsoft.com/61da7bc2-b805-4379-a6b2-1e92374be1a0">WsFreeError</a> 
                    are called for the error object.
                

To set the string value, pass a WS_XML_STRING* to <a href="https://msdn.microsoft.com/193664ab-4688-49c9-97e7-ccf2b3e2d7e8">WsSetFaultErrorProperty</a>.
                    The error object will make a copy of the string.
                

The default value is a zero-length string.
                


### -field WS_FAULT_ERROR_PROPERTY_HEADER

An optional <a href="https://msdn.microsoft.com/75f1df70-4dc9-4365-9005-5eaca6688f16">WS_XML_BUFFER</a> value representing a header to
                    add to the fault message relating to the fault.
                    If the pointer to the XML_BUFFER is <b>NULL</b>, then no header is present.
                

To get the header value, pass a WS_XML_BUFFER** to <a href="https://msdn.microsoft.com/b59e6ac6-a3f1-4a72-a941-f588950ba85a">WsGetFaultErrorProperty</a>.
                    The returned WS_XML_BUFFER is valid until <a href="https://msdn.microsoft.com/a01a65f1-3eca-452c-a10d-dc9c6c3db124">WsResetError</a> or <a href="https://msdn.microsoft.com/61da7bc2-b805-4379-a6b2-1e92374be1a0">WsFreeError</a> 
                    are called for the error object.
                

To set the header value, pass a WS_XML_BUFFER** to <a href="https://msdn.microsoft.com/193664ab-4688-49c9-97e7-ccf2b3e2d7e8">WsSetFaultErrorProperty</a>.
                    The error object will make a copy of the buffer.
                

The default value is <b>NULL</b>.
                

