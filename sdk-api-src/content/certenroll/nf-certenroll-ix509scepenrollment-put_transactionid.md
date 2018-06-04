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

# IX509SCEPEnrollment::put_TransactionId


## -description


Gets or sets the transaction id for the request.

This property is read/write.


## -parameters


## -remarks



If you do not specify a transaction id, then the <a href="https://msdn.microsoft.com/b86d6dc3-aa96-45f3-9551-f24c39ea6cbf">CreateRequestMessage</a> method will create one. If the transaction id has not been set or the <b>CreateRequestMessage</b>  method has not been called, then this property will return <b>CERTSRV_E_PROPERTY_EMPTY</b>.

After processing a pending request, the caller must save this value for later use when calling the <a href="https://msdn.microsoft.com/86d031b0-2009-460b-8bed-fe7a0489f22b">CreateRetrievePendingMessage</a> method to format a message to be sent to the SCEP server to poll for the issued certificate.

Set this property before you call the <a href="https://msdn.microsoft.com/4254fdf3-473f-4f22-a08f-13481fd9f779">ProcessResponseMessage</a> method when you are using a new instance of the <a href="https://msdn.microsoft.com/fcbac911-9e37-4994-bbb6-544b19a92749">IX509SCEPEnrollment</a> interface to install the response.

Set this property before you call the <a href="https://msdn.microsoft.com/86d031b0-2009-460b-8bed-fe7a0489f22b">CreateRetrievePendingMessage</a> method when you are using a new instance of the <a href="https://msdn.microsoft.com/fcbac911-9e37-4994-bbb6-544b19a92749">IX509SCEPEnrollment</a> interface to create a retrieval message.




## -see-also




<a href="https://msdn.microsoft.com/fcbac911-9e37-4994-bbb6-544b19a92749">IX509SCEPEnrollment</a>
 

 

