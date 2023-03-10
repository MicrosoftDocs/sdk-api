---
UID: NS:webservices._WS_VOID_DESCRIPTION
title: WS_VOID_DESCRIPTION (webservices.h)
description: Specifies information about a field which is neither serialized nor deserialized.
helpviewer_keywords: ["WS_VOID_DESCRIPTION","WS_VOID_DESCRIPTION structure [Web Services for Windows]","webservices/WS_VOID_DESCRIPTION","wsw.ws_void_description"]
old-location: wsw\ws_void_description.htm
tech.root: wsw
ms.assetid: 92373e0d-3fe1-4486-8e79-deb0fc24cb63
ms.date: 12/05/2018
ms.keywords: WS_VOID_DESCRIPTION, WS_VOID_DESCRIPTION structure [Web Services for Windows], webservices/WS_VOID_DESCRIPTION, wsw.ws_void_description
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
req.typenames: WS_VOID_DESCRIPTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_VOID_DESCRIPTION
 - webservices/_WS_VOID_DESCRIPTION
 - WS_VOID_DESCRIPTION
 - webservices/WS_VOID_DESCRIPTION
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
 - WS_VOID_DESCRIPTION
---

# WS_VOID_DESCRIPTION structure


## -description

Specifies information about a field which is neither serialized nor
                deserialized.
            

This is used with <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_VOID_TYPE</a> and <a href="/windows/desktop/api/webservices/ne-webservices-ws_field_mapping">WS_NO_FIELD_MAPPING</a> within a <a href="/windows/desktop/api/webservices/ns-webservices-ws_field_description">WS_FIELD_DESCRIPTION</a>.
            

This type description is only required when <a href="/windows/win32/api/webservices/ne-webservices-ws_xml_reader_encoding_type">WS_FIELD_POINTER</a> is not
                being used.

## -struct-fields

### -field size

The size of the field.