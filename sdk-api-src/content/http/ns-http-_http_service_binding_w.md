---
UID: NS:http._HTTP_SERVICE_BINDING_W
title: "_HTTP_SERVICE_BINDING_W"
author: windows-sdk-content
description: HTTP_SERVICE_BINDING_W.
old-location: http\http_service_binding_w.htm
old-project: http
ms.assetid: 0d840097-82d3-4ee3-b0d9-bcac4cf3e935
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PHTTP_SERVICE_BINDING_W, HTTP_SERVICE_BINDING_W, HTTP_SERVICE_BINDING_W structure [HTTP], PHTTP_SERVICE_BINDING_W, PHTTP_SERVICE_BINDING_W structure pointer [HTTP], _HTTP_SERVICE_BINDING_W, http.http_service_binding_w, http/HTTP_SERVICE_BINDING_W, http/PHTTP_SERVICE_BINDING_W"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: HTTP_SERVICE_BINDING_W, *PHTTP_SERVICE_BINDING_W
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Http.h
api_name:
 - HTTP_SERVICE_BINDING_W
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _HTTP_SERVICE_BINDING_W structure


## -description


The <b>HTTP_SERVICE_BINDING_W</b> structure provides  Service Principle Name (SPN) in Unicode. 


## -struct-fields




### -field Base

An <a href="https://msdn.microsoft.com/c9d3ed21-8987-4b98-99a1-dc1e776b0dab">HTTP_SERVICE_BINDING_BASE</a> value,  the <b>Type</b> member of which must be set to <b>HttpServiceBindingTypeW</b>.


### -field Buffer

A pointer to a buffer that represents the SPN.


### -field BufferSize

The length, in bytes, of the string in <b>Buffer</b>.

