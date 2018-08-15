---
UID: NS:webservices._WS_NETPIPE_URL
title: "_WS_NETPIPE_URL"
author: windows-sdk-content
description: The URL subtype for specifying an net.pipe URL.
old-location: wsw\ws_netpipe_url.htm
old-project: wsw
ms.assetid: A9B2C098-4420-490A-BB28-F8F1D3136225
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WS_NETPIPE_URL, WS_NETPIPE_URL structure [Web Services for Windows], _WS_NETPIPE_URL, webservices/_WS_NETPIPE_URL, wsw.ws_netpipe_url
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: webservices.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: WS_NETPIPE_URL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - _WS_NETPIPE_URL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_NETPIPE_URL structure


## -description


The URL subtype for specifying an net.pipe URL.
            


## -struct-fields




### -field url

The base type from which this URL subtype and all other URL subtypes derive. The <a href="https://msdn.microsoft.com/e8763719-6ba0-4e5e-bb71-625d36a45eaf">WS_URL_SCHEME_TYPE</a> is <b>WS_URL_NETPIPE_SCHEME_TYPE</b>.


### -field host

The host name.
                


### -field port

The port number.
                


### -field portAsString

The port number as string.
                


### -field path

The path.
                


### -field query

The query.
                


### -field fragment

The fragment.
                


## -remarks



If used with the <a href="https://msdn.microsoft.com/67147b71-ca3a-4a17-a4f1-6ba608eca742">WsDecodeUrl</a> field, <b>portAsString</b> is a zero-length string if no port is specified in <b>url</b>.
            




## -see-also




<a href="https://msdn.microsoft.com/4a7cf425-40c6-4951-880e-b3a99076bb2b">WS_HTTPS_URL</a>



<a href="https://msdn.microsoft.com/36f4dda6-d46a-44cd-b4cd-597fa3298870">WS_HTTP_URL</a>



<a href="https://msdn.microsoft.com/62079e59-01c8-48fb-932a-ca01cc7b86ec">WS_NETTCP_URL</a>



<a href="https://msdn.microsoft.com/f39c551f-891b-48c2-8143-84845506cde9">WS_SOAPUDP_URL</a>
 

 

