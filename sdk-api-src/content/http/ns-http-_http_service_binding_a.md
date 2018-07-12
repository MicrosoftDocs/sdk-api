---
UID: NS:http._HTTP_SERVICE_BINDING_A
title: "_HTTP_SERVICE_BINDING_A"
author: windows-sdk-content
description: HTTP_SERVICE_BINDING_A.
old-location: http\http_service_binding_a.htm
old-project: http
ms.assetid: bad1a042-fda8-4a2a-a8c1-26ed1f87c442
ms.author: windowssdkdev
ms.date: 04/13/2018
ms.keywords: "*PHTTP_SERVICE_BINDING_A, HTTP_SERVICE_BINDING_A, HTTP_SERVICE_BINDING_A structure [HTTP], PHTTP_SERVICE_BINDING_A, PHTTP_SERVICE_BINDING_A structure pointer [HTTP], _HTTP_SERVICE_BINDING_A, http.http_service_binding_a, http/HTTP_SERVICE_BINDING_A, http/PHTTP_SERVICE_BINDING_A"
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
req.typenames: HTTP_SERVICE_BINDING_A, *PHTTP_SERVICE_BINDING_A
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Http.h
api_name:
 - HTTP_SERVICE_BINDING_A
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _HTTP_SERVICE_BINDING_A structure


## -description


The <b>HTTP_SERVICE_BINDING_A</b> structure provides  Service Principle Name (SPN) in ASCII. 


## -struct-fields




### -field Base

An <a href="https://msdn.microsoft.com/c9d3ed21-8987-4b98-99a1-dc1e776b0dab">HTTP_SERVICE_BINDING_BASE</a> value,  the <b>Type</b> member of which must be set to <b>HttpServiceBindingTypeA</b>. 


### -field Buffer

A pointer to a buffer that represents the SPN.


### -field BufferSize

The length, in bytes, of the string in <b>Buffer</b>.

