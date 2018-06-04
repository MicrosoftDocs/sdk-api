---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# WINHTTP_CURRENT_USER_IE_PROXY_CONFIG structure


## -description


The <b>WINHTTP_CURRENT_USER_IE_PROXY_CONFIG</b> structure contains the Internet Explorer proxy configuration information.


## -struct-fields




### -field fAutoDetect

If TRUE, indicates that the Internet Explorer proxy configuration for the current user specifies "automatically detect settings".


### -field lpszAutoConfigUrl

Pointer to a null-terminated Unicode string that contains the auto-configuration URL if the Internet Explorer proxy configuration for the current user specifies "Use automatic proxy configuration".


### -field lpszProxy

Pointer to a null-terminated Unicode string that contains the proxy URL if the Internet Explorer proxy configuration for the current user specifies "use a proxy server".


### -field lpszProxyBypass

Pointer to a null-terminated Unicode string that contains the optional proxy by-pass server list.


## -see-also




<a href="https://msdn.microsoft.com/b69e5087-7849-4cbc-a97b-204a26fdd044">WinHTTP
		  Versions</a>
 

 

