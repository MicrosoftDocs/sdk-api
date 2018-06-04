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

# WS_URL_SCHEME_TYPE enumeration


## -description



                The set of schemes used with <a href="https://msdn.microsoft.com/67147b71-ca3a-4a17-a4f1-6ba608eca742">WsDecodeUrl</a>, <a href="https://msdn.microsoft.com/8253b062-072b-4d37-8b82-407df1bea6b4">WsEncodeUrl</a>, 
                and <a href="https://msdn.microsoft.com/6cff906a-adb7-4453-8d44-6a5bf44a681b">WsCombineUrl</a>.
            


## -enum-fields




### -field WS_URL_HTTP_SCHEME_TYPE


                    Denotes the "http" scheme: <a href="https://msdn.microsoft.com/36f4dda6-d46a-44cd-b4cd-597fa3298870">WS_HTTP_URL</a>



### -field WS_URL_HTTPS_SCHEME_TYPE


                    Denotes the "https" scheme: <a href="https://msdn.microsoft.com/4a7cf425-40c6-4951-880e-b3a99076bb2b">WS_HTTPS_URL</a>



### -field WS_URL_NETTCP_SCHEME_TYPE


                    Denotes the "net.tcp" scheme: <a href="https://msdn.microsoft.com/62079e59-01c8-48fb-932a-ca01cc7b86ec">WS_NETTCP_URL</a>



### -field WS_URL_SOAPUDP_SCHEME_TYPE


                    Denotes the "soap.udp" scheme: <a href="https://msdn.microsoft.com/f39c551f-891b-48c2-8143-84845506cde9">WS_SOAPUDP_URL</a>



### -field WS_URL_NETPIPE_SCHEME_TYPE

Windows 8 or later: Denotes the "net.pipe" scheme: <a href="https://msdn.microsoft.com/02FCD206-23BC-4ED0-9E4A-76AB0926FD7C">WS_NETPIPE_URL</a>


