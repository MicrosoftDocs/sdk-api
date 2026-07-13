---
UID: NE:http._HTTP_LOG_DATA_TYPE
title: HTTP_LOG_DATA_TYPE (http.h)
description: Identifies the type of log data.
helpviewer_keywords: ["*PHTTP_LOG_DATA_TYPE","*PHTTP_LOG_DATA_TYPE enumeration [HTTP]","HTTP_LOG_DATA_TYPE","HTTP_LOG_DATA_TYPE enumeration [HTTP]","HttpLogDataTypeFields","http.http_log_data_type","http/*PHTTP_LOG_DATA_TYPE","http/HTTP_LOG_DATA_TYPE","http/HttpLogDataTypeFields"]
old-location: http\http_log_data_type.htm
tech.root: http
ms.assetid: 8c53a3e6-5001-4e72-bff4-a6eab007aa9c
ms.date: 12/05/2018
ms.keywords: '*PHTTP_LOG_DATA_TYPE, *PHTTP_LOG_DATA_TYPE enumeration [HTTP], HTTP_LOG_DATA_TYPE, HTTP_LOG_DATA_TYPE enumeration [HTTP], HttpLogDataTypeFields, http.http_log_data_type, http/*PHTTP_LOG_DATA_TYPE, http/HTTP_LOG_DATA_TYPE, http/HttpLogDataTypeFields'
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
req.typenames: HTTP_LOG_DATA_TYPE, *PHTTP_LOG_DATA_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_LOG_DATA_TYPE
 - http/_HTTP_LOG_DATA_TYPE
 - PHTTP_LOG_DATA_TYPE
 - http/PHTTP_LOG_DATA_TYPE
 - HTTP_LOG_DATA_TYPE
 - http/HTTP_LOG_DATA_TYPE
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
 - HTTP_LOG_DATA_TYPE
---

# HTTP_LOG_DATA_TYPE enumeration


## -description

The <b>HTTP_LOG_DATA_TYPE</b> enumeration identifies the type of log data.

## -enum-fields

### -field HttpLogDataTypeFields:0

The <a href="/windows/desktop/api/http/ns-http-http_log_fields_data">HTTP_LOG_FIELDS_DATA</a> structure is used for logging a request. This structure is passed to an <a href="/windows/desktop/api/http/nf-http-httpsendhttpresponse">HttpSendHttpResponse</a> or <a href="/windows/desktop/api/http/nf-http-httpsendresponseentitybody">HttpSendResponseEntityBody</a> call.

## -see-also

<a href="/windows/desktop/api/http/ns-http-http_log_data">HTTP_LOG_DATA</a>
