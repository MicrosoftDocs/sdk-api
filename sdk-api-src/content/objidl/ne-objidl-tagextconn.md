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

# tagEXTCONN enumeration


## -description


Specifies the type of external connection existing on an embedded object. 


## -enum-fields




### -field EXTCONN_STRONG

The external connection is a link. If this value is specified, the external connection must keep the object alive until all strong external connections are cleared through <a href="https://msdn.microsoft.com/7ed598b2-9603-454a-99cf-849715e43ca1">IExternalConnection::ReleaseConnection</a>. 


### -field EXTCONN_WEAK

This value is not used.


### -field EXTCONN_CALLABLE

This value is not used.


## -see-also




<a href="https://msdn.microsoft.com/7439cb16-1da3-4fab-a16d-519f9ce1053a">IExternalConnection::AddConnection</a>



<a href="https://msdn.microsoft.com/7ed598b2-9603-454a-99cf-849715e43ca1">IExternalConnection::ReleaseConnection</a>
 

 

