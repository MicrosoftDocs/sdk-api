---
UID: NE:webservices.WS_COOKIE_MODE
title: WS_COOKIE_MODE
author: windows-sdk-content
description: An enumeration used to specify how to handle HTTP cookies.
old-location: wsw\ws_cookie_mode.htm
old-project: wsw
ms.assetid: d1430120-efaa-4af8-a669-720387c617b2
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WS_AUTO_COOKIE_MODE, WS_COOKIE_MODE, WS_COOKIE_MODE enumeration [Web Services for Windows], WS_MANUAL_COOKIE_MODE, webservices/WS_AUTO_COOKIE_MODE, webservices/WS_COOKIE_MODE, webservices/WS_MANUAL_COOKIE_MODE, wsw.ws_cookie_mode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: webservices.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: WS_COOKIE_MODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_COOKIE_MODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WS_COOKIE_MODE enumeration


## -description


An enumeration used to specify how to handle HTTP cookies.
            


## -enum-fields




### -field WS_MANUAL_COOKIE_MODE

In this mode, cookies are not processed by the client channel.
                

If a server sends a cookie to the client, the client
                    channel will ignore the cookie (it will not include
                    the cookie value in subsequent requests).
                

An application can use the <a href="https://msdn.microsoft.com/bca1f244-4692-42bb-bbd7-c96647038a06">WS_HTTP_HEADER_MAPPING</a>feature to handle cookies manually, if desired.
                


### -field WS_AUTO_COOKIE_MODE

In this mode, cookies are automatically tracked by
                    the channel.
                

If a server sends a cookie to the client,
                    the channel will automatically track the cookie and
                    will include the cookie in subsequent requests.
                

