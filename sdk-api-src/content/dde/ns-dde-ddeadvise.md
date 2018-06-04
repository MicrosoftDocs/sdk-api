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

# DDEADVISE structure


## -description


Contains flags that specify how a DDE server application should send data to a client application during an advise loop. A client passes a handle to a <b>DDEADVISE</b> structure to a server as part of a <a href="https://msdn.microsoft.com/b00db740-36a7-4487-abbf-d74b12f5212a">WM_DDE_ADVISE</a> message. 


## -struct-fields




### -field reserved

Type: <b>unsigned short</b>

Reserved.


### -field fDeferUpd

Type: <b>unsigned short</b>

Indicates whether the server should defer sending updated data to the client. If this value is nonzero, the server should send a <a href="https://msdn.microsoft.com/ed6a65d3-b2a3-45f2-9600-291ce2ec8c0a">WM_DDE_DATA</a> message with a <b>NULL</b> data handle whenever the data item changes. In response, the client can post a <a href="https://msdn.microsoft.com/922452d2-455c-43e1-a8a8-e3c52b0fab51">WM_DDE_REQUEST</a> message to the server to get a handle to the updated data. 


### -field fAckReq

Type: <b>short</b>

Indicates whether the server should set the <b>fAckReq</b> flag in the <a href="https://msdn.microsoft.com/ed6a65d3-b2a3-45f2-9600-291ce2ec8c0a">WM_DDE_DATA</a> messages it posts to the client. If this value is nonzero, the server should set the <b>fAckReq</b> bit. 


### -field usFlags

 


### -field cfFormat

Type: <b>short</b>

The client application's preferred data format. The format must be a standard or registered clipboard format. The following standard clipboard formats can be used: 
                



#### CF_BITMAP (2)



#### CF_DIB (8)



#### CF_DIF (5)



#### CF_ENHMETAFILE (14)



#### CF_METAFILEPICT (3)



#### CF_OEMTEXT (7)



#### CF_PALETTE (9)



#### CF_PENDATA (10)



#### CF_RIFF (11)



#### CF_SYLK (4)



#### CF_TEXT (1)



#### CF_TIFF (6)



#### CF_WAVE (12)



#### CF_UNICODETEXT (13)


## -see-also




<a href="https://msdn.microsoft.com/0bcd8de4-a6f0-4f2a-8b9d-0b1b638925fb">About Dynamic Data Exchange</a>



<b>Conceptual</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/b00db740-36a7-4487-abbf-d74b12f5212a">WM_DDE_ADVISE</a>



<a href="https://msdn.microsoft.com/ed6a65d3-b2a3-45f2-9600-291ce2ec8c0a">WM_DDE_DATA</a>



<a href="https://msdn.microsoft.com/9a5f9a86-e6fa-450e-b8bf-f20042c7e6d1">WM_DDE_UNADVISE</a>
 

 

