---
UID: NE:http._HTTP_503_RESPONSE_VERBOSITY
title: "_HTTP_503_RESPONSE_VERBOSITY"
author: windows-sdk-content
description: The HTTP_503_RESPONSE_VERBOSITY enumeration defines the verbosity levels for a 503, service unavailable, error responses.This structure must be used when setting or querying the HttpServer503ResponseProperty on a request queue.
old-location: http\http_503_response_verbosity.htm
old-project: http
ms.assetid: e103bdf4-dc48-45ba-84dc-4161310ee3ff
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PHTTP_503_RESPONSE_VERBOSITY, *PHTTP_503_RESPONSE_VERBOSITY enumeration [HTTP], HTTP_503_RESPONSE_VERBOSITY, HTTP_503_RESPONSE_VERBOSITY enumeration [HTTP], Http503ResponseVerbosityBasic, Http503ResponseVerbosityFull, Http503ResponseVerbosityLimited, _HTTP_503_RESPONSE_VERBOSITY, http.http_503_response_verbosity, http/*PHTTP_503_RESPONSE_VERBOSITY, http/HTTP_503_RESPONSE_VERBOSITY, http/Http503ResponseVerbosityBasic, http/Http503ResponseVerbosityFull, http/Http503ResponseVerbosityLimited"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: http.h
req.include-header: 
req.redist: 
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
req.typenames: HTTP_503_RESPONSE_VERBOSITY, *PHTTP_503_RESPONSE_VERBOSITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Http.h
api_name:
 - HTTP_503_RESPONSE_VERBOSITY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _HTTP_503_RESPONSE_VERBOSITY enumeration


## -description


The <b>HTTP_503_RESPONSE_VERBOSITY</b> enumeration defines the verbosity levels for a 503, service unavailable, error responses.

This structure must be used when setting or querying the <a href="https://msdn.microsoft.com/14865796-135c-43c2-955a-fdeae05a8278">HttpServer503ResponseProperty</a> on a request queue.


## -enum-fields




### -field Http503ResponseVerbosityBasic

A 503 response is not sent; the connection is reset.
    This is the default HTTP Server API behavior.


### -field Http503ResponseVerbosityLimited

The HTTP Server API sends a 503 response with a "Service Unavailable" reason phrase.


### -field Http503ResponseVerbosityFull

The HTTP Server API sends a 503 response with a detailed reason phrase.


## -remarks



This enumeration is used in <a href="https://msdn.microsoft.com/56111cc0-94c8-47dc-a3bb-ffc5dae772fe">HttpSetRequestQueueProperty</a>, and <a href="https://msdn.microsoft.com/a3b1e85e-f152-4038-a56a-3d5985757c45">HttpQueryrequestQueueProperty</a> to set and query the 503  response verbosity. The <i>pPropertyInformation</i> parameter points to a member of the <b>HTTP_503_RESPONSE_VERBOSITY</b> enumeration when the <i>Property</i> parameter is <b>HttpServer503VerbosityProperty</b>.

This enumeration defines the verbosity level for a request queue when sending 503 (Service Unavailable) error responses. Note that the 503 response level set using the <b>HTTP_503_RESPONSE_VERBOSITY</b>  enumeration only affects the error responses generated internally
 by the HTTP Server API.


<div class="alert"><b>Note</b>  Disclosing information about the state of the service to potentially unsafe clients may pose a security risk.</div>
<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/849b88a1-e60b-4a1d-a660-cc3fe429d39f">HTTP Server API Version 2.0 Enumeration Types</a>



<a href="https://msdn.microsoft.com/14865796-135c-43c2-955a-fdeae05a8278">HTTP_SERVER_PROPERTY</a>



<a href="https://msdn.microsoft.com/a3b1e85e-f152-4038-a56a-3d5985757c45">HttpQueryRequestQueueProperty</a>



<a href="https://msdn.microsoft.com/56111cc0-94c8-47dc-a3bb-ffc5dae772fe">HttpSetRequestQueueProperty</a>
 

 

