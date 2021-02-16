---
UID: NS:webservices._WS_CUSTOM_TYPE_DESCRIPTION
title: WS_CUSTOM_TYPE_DESCRIPTION (webservices.h)
description: Represents a custom mapping between a C data type and an XML element.
helpviewer_keywords: ["WS_CUSTOM_TYPE_DESCRIPTION","WS_CUSTOM_TYPE_DESCRIPTION structure [Web Services for Windows]","webservices/WS_CUSTOM_TYPE_DESCRIPTION","wsw.ws_custom_type_description"]
old-location: wsw\ws_custom_type_description.htm
tech.root: wsw
ms.assetid: 7ae3d16c-0755-4226-844e-52cf96fa84fb
ms.date: 12/05/2018
ms.keywords: WS_CUSTOM_TYPE_DESCRIPTION, WS_CUSTOM_TYPE_DESCRIPTION structure [Web Services for Windows], webservices/WS_CUSTOM_TYPE_DESCRIPTION, wsw.ws_custom_type_description
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
req.typenames: WS_CUSTOM_TYPE_DESCRIPTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_CUSTOM_TYPE_DESCRIPTION
 - webservices/_WS_CUSTOM_TYPE_DESCRIPTION
 - WS_CUSTOM_TYPE_DESCRIPTION
 - webservices/WS_CUSTOM_TYPE_DESCRIPTION
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
 - WS_CUSTOM_TYPE_DESCRIPTION
---

# WS_CUSTOM_TYPE_DESCRIPTION structure


## -description

Represents a custom mapping between a C data type and an XML element.User-defined callbacks are invoked to do the actual reading and
                writing.

## -struct-fields

### -field size

The size of the custom type, in bytes.

### -field alignment

The alignment requirement of the custom type.  This must be a
                    power of two between 1 and 8.

### -field readCallback

A pointer to a callback which is invoked to read the type.

### -field writeCallback

A pointer to a callback which is invoked to write the type.

### -field descriptionData

This can be used to point to additional user-defined data
                    specific to the type.  It is optional and may be <b>NULL</b>.
                

The pointer to this data is passed
                    to the <a href="/windows/desktop/api/webservices/nc-webservices-ws_read_type_callback">WS_READ_TYPE_CALLBACK</a> and the
                    <a href="/windows/desktop/api/webservices/nc-webservices-ws_write_type_callback">WS_WRITE_TYPE_CALLBACK</a>.  This allows the
                    callback to access information that is specific to this
                    particular usage of the callback.

### -field isDefaultValueCallback