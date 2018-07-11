---
UID: NS:http._HTTP_SERVER_AUTHENTICATION_BASIC_PARAMS
title: "_HTTP_SERVER_AUTHENTICATION_BASIC_PARAMS"
author: windows-sdk-content
description: The HTTP_SERVER_AUTHENTICATION_BASIC_PARAMS structure contains the information for Basic authentication on a URL Group.This structure is contained in the HTTP_SERVER_AUTHENTICATION_INFO structure.
old-location: http\http_server_authentication_basic_params.htm
old-project: http
ms.assetid: 02330a12-aab0-4181-b3da-36c6b22dae67
ms.author: windowssdkdev
ms.date: 04/13/2018
ms.keywords: "*PHTTP_SERVER_AUTHENTICATION_BASIC_PARAMS, *PHTTP_SERVER_AUTHENTICATION_BASIC_PARAMS structure [HTTP], HTTP_SERVER_AUTHENTICATION_BASIC_PARAMS, HTTP_SERVER_AUTHENTICATION_BASIC_PARAMS structure [HTTP], _HTTP_SERVER_AUTHENTICATION_BASIC_PARAMS, http.http_server_authentication_basic_params, http/*PHTTP_SERVER_AUTHENTICATION_BASIC_PARAMS, http/HTTP_SERVER_AUTHENTICATION_BASIC_PARAMS"
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
req.typenames: HTTP_SERVER_AUTHENTICATION_BASIC_PARAMS, *PHTTP_SERVER_AUTHENTICATION_BASIC_PARAMS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Http.h
api_name:
 - HTTP_SERVER_AUTHENTICATION_BASIC_PARAMS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _HTTP_SERVER_AUTHENTICATION_BASIC_PARAMS structure


## -description


The <b>HTTP_SERVER_AUTHENTICATION_BASIC_PARAMS</b> structure contains the information for Basic authentication on a URL Group.

This structure is contained in the <a href="https://msdn.microsoft.com/4f408115-c073-4e9f-b316-8ad3f03acf53">HTTP_SERVER_AUTHENTICATION_INFO</a> structure.


## -struct-fields




### -field RealmLength

The length, in bytes, of the <b>Realm</b> member.


### -field Realm

The realm used for Basic authentication.

The realm allows the  server to be partitioned into a set of protection spaces, each with its own set of authentication schemes from the authentication database.


## -see-also




<a href="https://msdn.microsoft.com/5a8e28e9-f85b-4550-929e-53f38eca6a8c">HTTP Server API Version 2.0 Structures</a>



<a href="https://msdn.microsoft.com/4f408115-c073-4e9f-b316-8ad3f03acf53">HTTP_SERVER_AUTHENTICATION_INFO</a>
 

 

