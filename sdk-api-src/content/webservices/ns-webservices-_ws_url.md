---
UID: NS:webservices._WS_URL
title: "_WS_URL"
author: windows-sdk-content
description: The abstract base type for all URL schemes used with WsDecodeUrl and WsEncodeUrl APIs.
old-location: wsw\ws_url.htm
tech.root: wsw
ms.assetid: efc67b64-cedf-4cd9-83b3-047f6c38c6ea
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: WS_URL, WS_URL structure [Web Services for Windows], _WS_URL, webservices/WS_URL, wsw.ws_url
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_URL
product: Windows
targetos: Windows
req.typenames: WS_URL
req.redist: 
---

# _WS_URL structure


## -description


The abstract base type for all URL schemes used with <a href="https://msdn.microsoft.com/67147b71-ca3a-4a17-a4f1-6ba608eca742">WsDecodeUrl</a> and <a href="https://msdn.microsoft.com/8253b062-072b-4d37-8b82-407df1bea6b4">WsEncodeUrl</a> APIs.
            


## -struct-fields




### -field scheme

A <a href="https://msdn.microsoft.com/e8763719-6ba0-4e5e-bb71-625d36a45eaf">WS_URL_SCHEME_TYPE</a> structure that describes the type of URL scheme.

