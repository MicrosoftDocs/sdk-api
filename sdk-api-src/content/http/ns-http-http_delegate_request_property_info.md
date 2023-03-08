---
UID: NS:http._HTTP_DELEGATE_REQUEST_PROPERTY_INFO
title: HTTP_DELEGATE_REQUEST_PROPERTY_INFO
description: Describes additional property information when delegating a request.
ms.date: 09/28/2020
tech.root: http
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: httpapi.dll
req.header: http.h
req.include-header: 
req.kmdf-ver: 
req.lib: httpapi.lib
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: HTTP_DELEGATE_REQUEST_PROPERTY_INFO, *PHTTP_DELEGATE_REQUEST_PROPERTY_INFO
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - httpapi.dll
api_name:
 - _HTTP_DELEGATE_REQUEST_PROPERTY_INFO
 - HTTP_DELEGATE_REQUEST_PROPERTY_INFO
f1_keywords:
 - http/_HTTP_DELEGATE_REQUEST_PROPERTY_INFO
 - http/HTTP_DELEGATE_REQUEST_PROPERTY_INFO
dev_langs:
 - c++
---

## -description

Describes additional property information when delegating a request.

## -struct-fields

### -field PropertyId

Type: **[HTTP_DELEGATE_REQUEST_PROPERTY_ID](./ne-http-http_delegate_request_property_id.md)**

The type of property info pointed to by this struct.

### -field PropertyInfoLength

Type: **[ULONG](/windows/win32/winprog/windows-data-types)**

The length in bytes of the value of the *PropertyInfo* parameter.

### -field PropertyInfo

Type: **[PVOID](/windows/win32/winprog/windows-data-types)**

A pointer to the property information.

## -remarks

## -see-also
