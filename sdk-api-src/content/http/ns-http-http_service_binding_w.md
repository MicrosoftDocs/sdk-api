---
UID: NS:http._HTTP_SERVICE_BINDING_W
title: HTTP_SERVICE_BINDING_W (http.h)
description: HTTP_SERVICE_BINDING_W.
helpviewer_keywords: ["*PHTTP_SERVICE_BINDING_W","HTTP_SERVICE_BINDING_W","HTTP_SERVICE_BINDING_W structure [HTTP]","PHTTP_SERVICE_BINDING_W","PHTTP_SERVICE_BINDING_W structure pointer [HTTP]","http.http_service_binding_w","http/HTTP_SERVICE_BINDING_W","http/PHTTP_SERVICE_BINDING_W"]
old-location: http\http_service_binding_w.htm
tech.root: http
ms.assetid: 0d840097-82d3-4ee3-b0d9-bcac4cf3e935
ms.date: 12/05/2018
ms.keywords: '*PHTTP_SERVICE_BINDING_W, HTTP_SERVICE_BINDING_W, HTTP_SERVICE_BINDING_W structure [HTTP], PHTTP_SERVICE_BINDING_W, PHTTP_SERVICE_BINDING_W structure pointer [HTTP], http.http_service_binding_w, http/HTTP_SERVICE_BINDING_W, http/PHTTP_SERVICE_BINDING_W'
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
req.typenames: HTTP_SERVICE_BINDING_W, *PHTTP_SERVICE_BINDING_W
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_SERVICE_BINDING_W
 - http/_HTTP_SERVICE_BINDING_W
 - PHTTP_SERVICE_BINDING_W
 - http/PHTTP_SERVICE_BINDING_W
 - HTTP_SERVICE_BINDING_W
 - http/HTTP_SERVICE_BINDING_W
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
 - HTTP_SERVICE_BINDING_W
---

# HTTP_SERVICE_BINDING_W structure


## -description

The <b>HTTP_SERVICE_BINDING_W</b> structure provides  Service Principle Name (SPN) in Unicode.

## -struct-fields

### -field Base

An <a href="/windows/desktop/api/http/ns-http-http_service_binding_base">HTTP_SERVICE_BINDING_BASE</a> value,  the <b>Type</b> member of which must be set to <b>HttpServiceBindingTypeW</b>.

### -field Buffer

A pointer to a buffer that represents the SPN.

### -field BufferSize

The length, in bytes, of the string in <b>Buffer</b>.