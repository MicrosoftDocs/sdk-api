---
UID: NC:webservices.WS_WRITE_TYPE_CALLBACK
title: WS_WRITE_TYPE_CALLBACK (webservices.h)
description: Invoked to write an element when WS_CUSTOM_TYPEhas been specified.
helpviewer_keywords: ["WS_WRITE_TYPE_CALLBACK","WS_WRITE_TYPE_CALLBACK callback","WS_WRITE_TYPE_CALLBACK callback function [Web Services for Windows]","webservices/WS_WRITE_TYPE_CALLBACK","wsw.ws_write_type_callback"]
old-location: wsw\ws_write_type_callback.htm
tech.root: wsw
ms.assetid: f94bdf80-abea-4a97-9d41-add498e314b1
ms.date: 12/05/2018
ms.keywords: WS_WRITE_TYPE_CALLBACK, WS_WRITE_TYPE_CALLBACK callback, WS_WRITE_TYPE_CALLBACK callback function [Web Services for Windows], webservices/WS_WRITE_TYPE_CALLBACK, wsw.ws_write_type_callback
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_WRITE_TYPE_CALLBACK
 - webservices/WS_WRITE_TYPE_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WebServices.h
api_name:
 - WS_WRITE_TYPE_CALLBACK
---

# WS_WRITE_TYPE_CALLBACK callback function


## -description

Invoked to write an element when <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_CUSTOM_TYPE</a> has been specified.  This allows writing of XML constructs which do not easily
                map to the core serialization model.

## -parameters

### -param writer [in]

A  <b>WS_XML_WRITER</b> pointer to the writer that the value should be written to.

### -param typeMapping [in]

Indicates how the XML is being mapped to this type.  See <a href="/windows/desktop/api/webservices/ne-webservices-ws_type_mapping">WS_TYPE_MAPPING</a> for more information.
                

If a mapping does not make sense for this particular type, the callback
                    should return <b>WS_E_INVALID_OPERATION</b>. (See <a href="/windows/desktop/wsw/windows-web-services-return-values">Windows Web Services Return Values</a>.)  A callback implementation
                    should be prepared to be passed new mapping types in future versions and should return
                    <b>WS_E_INVALID_OPERATION</b> for those cases.

### -param descriptionData [in]

This is the value of the <b>descriptionData</b> field of the <a href="/windows/desktop/api/webservices/ns-webservices-ws_custom_type_description">WS_CUSTOM_TYPE_DESCRIPTION</a> structure.
                    The callback uses this field to access any additional information about the type.

### -param value

A  <b>void</b> pointer to a value to serialize.

### -param valueSize [in]

The size, in bytes, of the value being serialized.

### -param error [in, optional]

A pointer to a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> data structure where additional error information should be stored if the function fails.

## -returns

This callback function does not return a value.

## -remarks

The callback will be invoked with the same calling sequence as
                <a href="/windows/desktop/api/webservices/nf-webservices-wswritetype">WsWriteType</a> in the documentation for <a href="/windows/desktop/api/webservices/ne-webservices-ws_type_mapping">WS_TYPE_MAPPING</a>.
                This defines what parts of the XML that the callback should write.
