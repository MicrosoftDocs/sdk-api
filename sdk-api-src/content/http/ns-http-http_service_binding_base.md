---
UID: NS:http._HTTP_SERVICE_BINDING_BASE
title: HTTP_SERVICE_BINDING_BASE (http.h)
description: HTTP_SERVICE_BINDING_BASE.
helpviewer_keywords: ["*PHTTP_SERVICE_BINDING_BASE","HTTP_SERVICE_BINDING_BASE","HTTP_SERVICE_BINDING_BASE structure [HTTP]","PHTTP_SERVICE_BINDING_BASE","PHTTP_SERVICE_BINDING_BASE structure pointer [HTTP]","http.http_service_binding_base","http/HTTP_SERVICE_BINDING_BASE","http/PHTTP_SERVICE_BINDING_BASE"]
old-location: http\http_service_binding_base.htm
tech.root: http
ms.assetid: c9d3ed21-8987-4b98-99a1-dc1e776b0dab
ms.date: 12/05/2018
ms.keywords: '*PHTTP_SERVICE_BINDING_BASE, HTTP_SERVICE_BINDING_BASE, HTTP_SERVICE_BINDING_BASE structure [HTTP], PHTTP_SERVICE_BINDING_BASE, PHTTP_SERVICE_BINDING_BASE structure pointer [HTTP], http.http_service_binding_base, http/HTTP_SERVICE_BINDING_BASE, http/PHTTP_SERVICE_BINDING_BASE'
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
req.typenames: HTTP_SERVICE_BINDING_BASE, *PHTTP_SERVICE_BINDING_BASE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_SERVICE_BINDING_BASE
 - http/_HTTP_SERVICE_BINDING_BASE
 - PHTTP_SERVICE_BINDING_BASE
 - http/PHTTP_SERVICE_BINDING_BASE
 - HTTP_SERVICE_BINDING_BASE
 - http/HTTP_SERVICE_BINDING_BASE
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
 - HTTP_SERVICE_BINDING_BASE
---

# HTTP_SERVICE_BINDING_BASE structure


## -description

The <b>HTTP_SERVICE_BINDING_BASE</b> structure is a placeholder for the <a href="/windows/desktop/api/http/ns-http-http_service_binding_a">HTTP_SERVICE_BINDING_A</a> structure and the <a href="/windows/desktop/api/http/ns-http-http_service_binding_w">HTTP_SERVICE_BINDING_W</a> structure.

## -struct-fields

### -field Type

Pointer to an <a href="/windows/desktop/api/http/ne-http-http_service_binding_type">HTTP_SERVICE_BINDING_TYPE</a> value that indicates whether the data is in ASCII or Unicode.

## -remarks

<div class="alert"><b>Note</b>  <p class="note">The first member of both the  <a href="/windows/desktop/api/http/ns-http-http_service_binding_a">HTTP_SERVICE_BINDING_A</a> structure and the <a href="/windows/desktop/api/http/ns-http-http_service_binding_w">HTTP_SERVICE_BINDING_W</a> structure is a <b>HTTP_SERVICE_BINDING_BASE</b> structure.  Therefore, an array of either of the first two structures can be indicated by a pointer to a <b>HTTP_SERVICE_BINDING_BASE</b> structure.

<p class="note">The <b>ServiceNames</b> member of the <a href="/windows/desktop/api/http/ns-http-http_channel_bind_info">HTTP_CHANNEL_BIND_INFO</a> structure is cast to a  pointer to a <b>HTTP_SERVICE_BINDING_BASE</b> structure for this purpose.

</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/http/ns-http-http_channel_bind_info">HTTP_CHANNEL_BIND_INFO</a>



<a href="/windows/desktop/api/http/ns-http-http_service_binding_a">HTTP_SERVICE_BINDING_A</a>



<a href="/windows/desktop/api/http/ne-http-http_service_binding_type">HTTP_SERVICE_BINDING_TYPE</a>



<a href="/windows/desktop/api/http/ns-http-http_service_binding_w">HTTP_SERVICE_BINDING_W</a>