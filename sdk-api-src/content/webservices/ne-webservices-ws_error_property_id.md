---
UID: NE:webservices.__unnamed_enum_30
title: WS_ERROR_PROPERTY_ID (webservices.h)
description: A set of property values associated with the error. They are set and retrieved using WsGetErrorProperty and WsSetErrorProperty.
helpviewer_keywords: ["WS_ERROR_PROPERTY_ID","WS_ERROR_PROPERTY_ID enumeration [Web Services for Windows]","WS_ERROR_PROPERTY_LANGID","WS_ERROR_PROPERTY_ORIGINAL_ERROR_CODE","WS_ERROR_PROPERTY_STRING_COUNT","webservices/WS_ERROR_PROPERTY_ID","webservices/WS_ERROR_PROPERTY_LANGID","webservices/WS_ERROR_PROPERTY_ORIGINAL_ERROR_CODE","webservices/WS_ERROR_PROPERTY_STRING_COUNT","wsw.ws_error_property_id"]
old-location: wsw\ws_error_property_id.htm
tech.root: wsw
ms.assetid: 527e39be-c959-40db-8f0b-14dcd49a7ca7
ms.date: 12/05/2018
ms.keywords: WS_ERROR_PROPERTY_ID, WS_ERROR_PROPERTY_ID enumeration [Web Services for Windows], WS_ERROR_PROPERTY_LANGID, WS_ERROR_PROPERTY_ORIGINAL_ERROR_CODE, WS_ERROR_PROPERTY_STRING_COUNT, webservices/WS_ERROR_PROPERTY_ID, webservices/WS_ERROR_PROPERTY_LANGID, webservices/WS_ERROR_PROPERTY_ORIGINAL_ERROR_CODE, webservices/WS_ERROR_PROPERTY_STRING_COUNT, wsw.ws_error_property_id
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
targetos: Windows
req.typenames: WS_ERROR_PROPERTY_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_ERROR_PROPERTY_ID
 - webservices/WS_ERROR_PROPERTY_ID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_ERROR_PROPERTY_ID
---

# WS_ERROR_PROPERTY_ID enumeration


## -description

A set of property values associated with the error.  They are set
                and retrieved using <a href="/windows/desktop/api/webservices/nf-webservices-wsgeterrorproperty">WsGetErrorProperty</a> and 
                <a href="/windows/desktop/api/webservices/nf-webservices-wsseterrorproperty">WsSetErrorProperty</a>.

## -enum-fields

### -field WS_ERROR_PROPERTY_STRING_COUNT:0

The number of error strings (ULONG) available in the error object. Error strings 
                    might be added using <a href="/windows/desktop/api/webservices/nf-webservices-wsadderrorstring">WsAddErrorString</a>. When <a href="/windows/desktop/api/webservices/ne-webservices-ws_error_property_id">WS_ERROR_PROPERTY_ORIGINAL_ERROR_CODE</a> is present in the error object, the corresponding error text will be counted as an
                    additional string in the returned number of error strings. 
                

                    This property is read only.

### -field WS_ERROR_PROPERTY_ORIGINAL_ERROR_CODE:1

If the error returned from the function was mapped to one of the 
                    standard WS_E_* errors, then this property is used to store the original
                    implementation specific error code.
                

Note that the original error code is specific to a particular implementation and version of the underlying libraries used by WWSAPI. It should not be 
                    expected to remain constant, as the libraries may change.  


The main purpose in exposing this error is for diagnostic purposes, as the application may
                    take a look at original error code of underlying library that caused this error.


Applications that take specific action based on the implementation
                    specific error code will likely be broken when the implementation changes.
                

If the error was not mapped from an implementation specific value 
                    to a standard error, then this property will have the value NOERROR.                
                

The default value is NOERROR.

### -field WS_ERROR_PROPERTY_LANGID:2

This identifies the language of any language sensitive information
                    in the error object.
                

This value may not be zero.
                

This value may only be set when the error object is first created, or
                    after it has been reset using <a href="/windows/desktop/api/webservices/nf-webservices-wsreseterror">WsResetError</a>.
