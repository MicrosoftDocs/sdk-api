---
UID: NS:http._HTTP_SERVICE_BINDING_A
title: HTTP_SERVICE_BINDING_A (http.h)
description: HTTP_SERVICE_BINDING_A.
helpviewer_keywords: ["*PHTTP_SERVICE_BINDING_A","HTTP_SERVICE_BINDING_A","HTTP_SERVICE_BINDING_A structure [HTTP]","PHTTP_SERVICE_BINDING_A","PHTTP_SERVICE_BINDING_A structure pointer [HTTP]","http.http_service_binding_a","http/HTTP_SERVICE_BINDING_A","http/PHTTP_SERVICE_BINDING_A"]
old-location: http\http_service_binding_a.htm
tech.root: http
ms.assetid: bad1a042-fda8-4a2a-a8c1-26ed1f87c442
ms.date: 12/05/2018
ms.keywords: '*PHTTP_SERVICE_BINDING_A, HTTP_SERVICE_BINDING_A, HTTP_SERVICE_BINDING_A structure [HTTP], PHTTP_SERVICE_BINDING_A, PHTTP_SERVICE_BINDING_A structure pointer [HTTP], http.http_service_binding_a, http/HTTP_SERVICE_BINDING_A, http/PHTTP_SERVICE_BINDING_A'
req.header: http.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: HTTP_SERVICE_BINDING_A, *PHTTP_SERVICE_BINDING_A
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_SERVICE_BINDING_A
 - http/_HTTP_SERVICE_BINDING_A
 - PHTTP_SERVICE_BINDING_A
 - http/PHTTP_SERVICE_BINDING_A
 - HTTP_SERVICE_BINDING_A
 - http/HTTP_SERVICE_BINDING_A
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Http.h
api_name:
 - HTTP_SERVICE_BINDING_A
---

# HTTP_SERVICE_BINDING_A structure


## -description

The <b>HTTP_SERVICE_BINDING_A</b> structure provides  Service Principle Name (SPN) in ASCII.

## -struct-fields

### -field Base

An <a href="/windows/desktop/api/http/ns-http-http_service_binding_base">HTTP_SERVICE_BINDING_BASE</a> value,  the <b>Type</b> member of which must be set to <b>HttpServiceBindingTypeA</b>.

### -field Buffer

A pointer to a buffer that represents the SPN.

### -field BufferSize

The length, in bytes, of the string in <b>Buffer</b>.