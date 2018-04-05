---
UID: NE:http._HTTP_ENABLED_STATE
title: "_HTTP_ENABLED_STATE"
author: windows-driver-content
description: Defines the state of a request queue, server session, or URL Group.
old-location: http\http_enabled_state.htm
old-project: Http
ms.assetid: 15e27788-2d1a-4818-b31f-2faf649e15b2
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: "*PHTTP_ENABLED_STATE, *PHTTP_ENABLED_STATE enumeration [HTTP], HTTP_ENABLED_STATE, HTTP_ENABLED_STATE enumeration [HTTP], HttpEnabledStateActive, HttpEnabledStateInactive, _HTTP_ENABLED_STATE, http.http_enabled_state, http/*PHTTP_ENABLED_STATE, http/HTTP_ENABLED_STATE, http/HttpEnabledStateActive, http/HttpEnabledStateInactive"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: HTTP_ENABLED_STATE, *PHTTP_ENABLED_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Http.h
api_name:
-	HTTP_ENABLED_STATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _HTTP_ENABLED_STATE enumeration


## -description


The <b>HTTP_ENABLED_STATE</b> enumeration defines the state of a request queue, server session, or URL Group.

This enumeration is used in the <a href="https://msdn.microsoft.com/736ae89b-a4fb-4962-ae68-9aaccd869c88">HTTP_STATE_INFO</a> struct


## -enum-fields




### -field HttpEnabledStateActive

The HTTP Server API object is enabled.


### -field HttpEnabledStateInactive

The HTTP Server API object is disabled.


## -remarks



 The default state of a request queue is enabled. Typically this enumeration is used to temporarily disable a request queue.




## -see-also




<a href="https://msdn.microsoft.com/849b88a1-e60b-4a1d-a660-cc3fe429d39f">HTTP Server API Version 2.0 Enumeration Types</a>



<a href="https://msdn.microsoft.com/736ae89b-a4fb-4962-ae68-9aaccd869c88">HTTP_STATE_INFO</a>
 

 

